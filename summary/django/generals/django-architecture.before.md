---
alwaysApply: false
---
## Layered Architecture (Project Standard)

### Layers

- **Controller (APIView)**: Request parsing, serializer validation, response mapping. No ORM/business logic.
- **Service**: Business rules, authorization, transactions, orchestration. The only layer allowed to call repositories/models.
- **Repository (optional)**: Encapsulate ORM queries and persistence.
- **Model**: Domain state and intrinsic validation.

### Golden Rules

- Views/serializers must not import models or repositories.
- Serializers never execute queries for validation.
- Services expose clear methods (e.g., `create`, `update`, `list`, `retrieve`, `delete`).
- Services raise domain-specific errors carrying HTTP status hints.

### Example Wiring

```python
# controller.py
class ThingCreateAPIView(APIView):
    def post(self, request):
        s = ThingCreateSerializer(data=request.data)
        s.is_valid(raise_exception=True)
        try:
            obj = ThingService.create(s.validated_data, user=request.user)
        except ServiceError as e:
            return Response({"detail": str(e)}, status=e.status_code)
        return Response(ThingReadSerializer(obj).data, status=201)

# services.py
class ThingService:
    @staticmethod
    def create(data: dict, user) -> Thing:
        with transaction.atomic():
            # business rules + repository calls
            return ThingRepository.create(data | {"owner": user})

# repositories.py
class ThingRepository:
    @staticmethod
    def create(data: dict) -> Thing:
        return Thing.objects.create(**data)
```

### Prohibited

- Model/ViewSet/Generic CBV that directly reference models.
- Business logic in views/serializers or middleware.

## Practical Layer Guide (Integrated)

아래는 Django를 **utils / serializer / service / validationservice / repository / model / view** 로 나눌 때의 역할, “직접 참조 금지” 규칙, 그리고 **Generic BaseRepository** 상속 규약까지 묶은 실무용 요약입니다.
불필요한 장황함 없이, 정확한 의존성·라이프사이클 기준만 정리합니다.

Note: This project standardizes on DRF APIView controllers (no ViewSets) for HTTP endpoints. Any mentions of ViewSet below are general guidance; in this codebase use APIView.

---

# 1) 레이어 역할 요약

* **Model**

  * DB 테이블과 1:1 매핑되는 도메인 엔티티.
  * 필드 제약(유니크, 널, choices)과 최소한의 도메인 불변식만.
  * 비즈니스 플로우/트랜잭션 로직 금지.

* **Repository**

  * 특정 Model에 대한 **영속성 계층**(ORM 캡슐화).
  * CRUD, 조회 최적화(select_related, prefetch_related), 잠금(select_for_update) 등 **데이터 접근 전담**.
  * 비즈니스 규칙·상태 전이 로직 금지.

* **ValidationService**

  * **모델 단일 필드를 넘어서는 도메인 규칙 검증**(예: 환불 가능 상태, 보유권한, 한도, 교차 엔티티 제약).
  * I/O 변환이 아닌 **비즈니스 규칙 평가**만 담당. 부수효과 금지(쓰기, 알림 전송 등).

* **Service**

  * **유즈케이스 오케스트레이션**(여러 Repository 호출 + ValidationService 검증 + 트랜잭션 경계).
  * 상태 전이, 도메인 이벤트 발행, 감사 로그 등 **비즈니스 중심**.
  * HTTP/직렬화 포맷 인지 금지.

* **Serializer (DRF)**

  * **입력 파싱→validated_data / 출력 직렬화→.data** 전담.
  * 필드 수준의 단순 검증만. 복합 도메인 규칙은 ValidationService로 위임.
  * DB 접근·비즈니스 전이 금지.

* **View (DRF View/APIView/ViewSet)**

  * HTTP 엔드포인트: 인증/권한, Serializer 바인딩, Service 호출, 응답 생성.
  * 도메인 로직 금지.

* **Utils**

  * 도메인 독립적 순수 함수(날짜/문자열/이미지/해시 등). 상태 전이·DB 접근 금지.

---

# 2) “직접 참조 금지” 매트릭스

| From \\ To             | Utils | Serializer | ValidationService |    Repository |         Model |  Service |     View |
| --------------------- | ----: | ---------: | ----------------: | ------------: | ------------: | -------: | -------: |
| **Utils**             |     ✅ |         🚫 |                🚫 |            🚫 |            🚫 |       🚫 |       🚫 |
| **Serializer**        |     ✅ |   ✅(자기 내부) |          ✅(규칙 위임) |            🚫 |            🚫 |       🚫 |       🚫 |
| **ValidationService** |     ✅ |         🚫 |       ✅(내부 호출 OK) |             ✅ |   ✅(타입/상수 참조) |       🚫 |       🚫 |
| **Repository**        |     ✅ |         🚫 |                🚫 | ✅(자기/협력 Repo) |             ✅ |       🚫 |       🚫 |
| **Service**           |     ✅ |         🚫 |                 ✅ |             ✅ |      ✅(타입/상수) | ✅(내부 헬퍼) |       🚫 |
| **View**              |     ✅ |          ✅ |                 ✅ |             ✅ | 🚫(직접 ORM 금지) |        ✅ | ✅(프레임워크) |

* 핵심 금지:

  * **View↔Model 직접쿼리 금지**, **Serializer↔Repository 직접호출 금지**, **Service↔Serializer 상호의존 금지**.
  * **Repository는 비즈니스 판단 금지**, **ValidationService는 쓰기/부수효과 금지**.

---

# 3) 라이프사이클(요청→응답) 흐름

`View → Serializer(입력 파싱) → ValidationService(규칙검증) → Service(트랜잭션·상태전이) → Repository(DB) → Service → Serializer(출력) → View(Response)`

* 트랜잭션 경계는 **Service**가 잡는다(`@transaction.atomic`).
* Repository는 **DB I/O만**, ValidationService는 **규칙만**, Serializer는 **변환만**.

---

# 4) BaseRepository(Generic) 규약

아래 코드는 잘 잡혀 있습니다. 실무에서 추가하면 좋은 규약만 덧붙입니다.

## 4.1 필수 규약

* **단일 모델당 하나의 Repo**: `UserSocialAccountRepository(BaseRepository[UserSocialAccount])`.
* **반환 타입 명확화**: `Optional[T]`, `QuerySet[T]` 표기.
* **읽기 전용과 쓰기 메서드 분리 네이밍**: `find_/get_/list_` vs `create/update/delete`.
* **존재 확인/중복 방지**: `exists_*`, `get_or_create_*`, `update_or_create_*`.
* **성능 최적화 포인트**: `select_related`, `prefetch_related`, `only/defer`, 배치 `bulk_create/bulk_update`.
* **잠금**(경합 도메인): 서비스에서 `select_for_update()` 메서드 제공.

## 4.2 개선 예시(패턴)

* **검색/조회 계층화**

  * `get_by_id(pk)`는 **없으면 None** 리턴(서비스에서 에러 매핑).
  * “없으면 예외”가 필요한 경우는 **Service에서** 예외 변환.

* **쓰기 안전성**

  * `update(instance, **fields)`는 변경 필드만 `update_fields`에 반영(이미 구현 OK).
  * 대량 업데이트는 `QuerySet.update()` 별도 메서드로 노출.

* **일관된 에러 처리**

  * Repo는 ORM 예외를 **누설하지 않거나**(None 반환), **Repo 전용 예외**로 매핑.
  * 서비스는 이를 도메인 예외/HTTP 에러로 최종 매핑.

* **슬라이스/페이지네이션**

  * `paginate(filters, page, size) -> Page[T]` 같은 얇은 래퍼 제공(뷰가 직접 쿼리셋 슬라이스 금지).

---

# 5) ValidationService vs Serializer 검증 경계

* **Serializer**: 형식 검증(필수/타입/범위), 간단한 교차 필드 확인 수준.
* **ValidationService**: 도메인 규칙(예: “이미 구매한 에피소드는 재구매 불가”, “환불 기한 7일 제한”, “보유 포인트 충분해야 함”).
* **의존성**: ValidationService는 **Repository**에서 읽고 판단만 하며, **Service**가 그 결과를 바탕으로 상태 전이를 실행.

---

# 6) Service 규약(트랜잭션·오케스트레이션)

* **트랜잭션 경계**: 유즈케이스 단위(`@transaction.atomic`).
* **잠금 필요 시**: Repo에 `get_for_update(...)` 같은 메서드 두고 Service가 호출.
* **이벤트/알림**: 외부 IO는 트랜잭션 커밋 후 훅(post-commit)에서 발행(이중 실행 방지).
* **입출력 포맷 무지**: 요청/응답 포맷은 Serializer가 담당.

---

# 7) View & Serializer 규약(HTTP 경계)

* **View**

  * 인증/권한 → 입력 Serializer로 파싱 → ValidationService 호출(필요시) → Service 실행 → 출력 Serializer 응답.
  * ORM/Repo 직접 호출 금지(테스트가 어려워짐).

* **Serializer**

  * `.is_valid()`로 입력 파싱/형식 검증 후, **도메인 검증은 위임**.
  * `.save()` 커스터마이즈로 Service 호출을 유도하지 말고, **View에서 Service를 명시 호출**(의존성 숨김 방지).

---

# 8) Utils 규약

* **순수 함수**만(입력→출력, 부수효과/상태 없음).
* 도메인 캡슐화된 상수/정책값 참조 금지(그건 ValidationService/Service가 소유).

---

# 9) 디렉터리 예시(간결형)

```
app/
  models/
    user_social_account.py
  repositories/
    base.py
    user_social_account.py
  services/
    purchase_service.py
    refund_service.py
  validations/
    purchase_rules.py
  serializers/
    purchase.py
    account.py
  views/
    purchase_view.py
  utils/
    dates.py
    images.py
```

---

# 10) 제공하신 Repository 코드에 대한 코멘트(간단)

* 현재 구조는 **바람직**합니다. 다음 보완을 추천드립니다.

  1. `get_for_update(pk)` 제공(경합 도메인에 필수).
  2. `exists_*`, `get_or_create_*` 추가로 **중복·경합** 방어.
  3. 읽기 최적화 메서드(예: `list_with_relations()`)에서 `select_related/prefetch_related` 내장.
  4. 예외 노출 정책 일관화(없음→`None`, 나머지 ORM 예외는 RepoException 등으로 변환).
  5. 반환 타입 주석 강화(`QuerySet[ModelT]`, `Optional[ModelT]`)로 정적 타이핑 이득 극대화.

---


