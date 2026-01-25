---
name: writing-plans
description: Executable implementation plans for complex dev/refactor/architecture; use when spec or requirements exist for multi-step work, before coding. Senior engineer/architect role. Bite-sized tasks (2–5 min/step), TDD, exact paths, save to docs/plans/.
---

# Writing Plans

## Role & When to Use

**Role:** 시니어 엔지니어/아키텍트. **실행 가능한 계획** — 말이 아니라 바로 작업에 투입할 수 있는 수준.

**When:** 스펙/요구사항이 있는 **다단계 작업**, **코드 작성 전**. 제로 컨텍스트 엔지니어가 따라할 수 있게.

**Announce:** "I'm using the writing-plans skill to create the implementation plan."

**Save to:** `docs/plans/YYYY-MM-DD-<feature-name>.md`

---

## Plan Header (필수)

**모든 계획은 아래 헤더로 시작:**

```markdown
# [Feature Name] Implementation Plan

> **For Claude:** Use superpowers:executing-plans to implement this plan task-by-task.

**Goal:** [한 문장]

**Architecture:** [2–3문장]

**Tech Stack:** [주요 기술/라이브러리]

---
```

---

## 프로젝트/문제 컨텍스트 (필수)

> 이 섹션이 비어 있으면 계획을 세울 수 없다.

- **시스템 개요:** 프로젝트명, 핵심 도메인, 기술 스택
- **현재 상황:** [문제/요구사항], [관련 코드/모듈], [제약], [기존 시도 및 결과]

---

## 원칙

### 작업 분리
- **적절한 분리:** 비즈니스 로직·서비스·배포 단위 등 의미 있는 단위만
- **과도한 분리 금지:** 단순 함수·한 곳만 쓰는 요소는 상위에 포함
- **기능/행동 보존:** 리팩토링 시 외부 동작 동일

### 계획 수립
- **불확실성:** 확신 없으면 `🔍 조사 필요`
- **구체화:** 추상 슬로건 금지, 현실적 작업 단위로 분해
- **의존성:** `→` 또는 `blocks:` / `depends_on:` 명시
- **목표 연결:** 각 작업이 궁극 목표에 어떻게 기여하는지

### Bite-sized & TDD (writing-plans)
- **한 스텝 = 2–5분:** "failing test" → "실패 확인" → "최소 구현" → "통과 확인" → "커밋" 각각 별도 스텝
- **Exact file paths**, **완전한 코드** ( "add validation" 같은 추상 표현 금지), **정확한 명령·기대 결과**
- **DRY, YAGNI, TDD, frequent commits**

### 금지
- 과도한 최적화, 과도하게 방어적인 코드, `getattr`/`setattr`/`hasattr` 등 동적 코드

---

## 출력 형식

### 1. 요약 (3–5줄)

### 2. 궁극적인 목표 + 측정 기준

| 목표     | 측정 기준 |
| -------- | --------- |
| (예시)   | (예시)    |

### 3. 작업 목록 [P1]… + Task/Steps

**작업 단위 [P1] (plan 스타일):**

```markdown
## [P1] 작업명 - 상태: 🔴 대기 | 🟡 진행중 | 🟢 완료 | ⛔ 블로킹

**목적 / 목표 연결 / 의존성** (`depends_on:` 또는 `blocks:`)

**주요 변경 지점 (정확한 경로):**
- Create: `path/to/file.py`
- Modify: `path/to/file.py:123-145`
- Test: `tests/path/test.py`

**예상 난이도·리스크·롤백·완료 기준**
```

**TDD 진행 시 각 [P1] 내 Step (writing-plans):**

- **Step 1:** failing test (코드 전체)
- **Step 2:** 실행·실패 확인 (명령 + 기대 FAIL)
- **Step 3:** 최소 구현 (코드)
- **Step 4:** 실행·통과 확인 (명령 + 기대 PASS)
- **Step 5:** `git add` / `git commit -m "..."`

### 4. 의존성 다이어그램

```
P0 → P1, P2 → P3 …
```

### 5. 조사 필요 항목 (선택)

| 항목 | 조사 이유 | 방법 | 결정 기준 |

### 6. 검증/완료 기준

- [ ] P* 전부 🟢, 기존 테스트 통과, 신규 테스트, 성능 등

---

## 다른 모델/세션 전달용

```markdown
## 📌 컨텍스트 요약

### 진행: 완료 / 진행중 / 블로킹
### 핵심 결정·주의사항·인수인계
```

---

## Execution Handoff

계획 저장 후:

**"Plan saved to `docs/plans/<filename>.md`. 실행 방식:**

**1. Subagent (이 세션)** — superpowers:subagent-driven-development, 태스크마다 서브에이전트 + 리뷰

**2. 별도 세션** — worktree 새 세션에서 superpowers:executing-plans

**Which?"**

---

## 예시 (통합)

```markdown
## [P1] STT 캐싱 레이어 - 🔴 대기

**목적:** 동일 오디오 재변환 방지, API 비용 절감  
**의존성:** `depends_on: []`  
**변경:** Create `transcription/repositories/stt_cache_repository.py`, Modify `transcription/services/stt_service.py`  
**완료 기준:** 캐시 히트/미스·기존 STT 테스트 통과

**Step 1: failing test**  
`tests/.../test_stt_cache.py`에 `test_cache_hit_skips_api` (기대: 호출 0회)  
**Step 2:** `pytest tests/.../test_stt_cache.py::test_... -v` → FAIL (함수/경로 없음)  
**Step 3–5:** 최소 구현 → PASS → commit
```

---

**우선 "프로젝트/문제 컨텍스트"를 채운 뒤, 위 형식으로 계획을 세운다.**
