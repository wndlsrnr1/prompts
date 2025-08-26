# 🧠 Enhanced Universal Reasoning Framework v2.1
**SOURCE VERIFICATION ENHANCEMENT**: 강화된 소스 검증 메커니즘

## ⚡ **Phase 1: 소스 검증 메커니즘 강화**

### 🎯 **Step 1.1: 원본 데이터 추적 시스템**

#### 소스 계층화 프로토콜 (MANDATORY)
```source-hierarchy
SOURCE_PRIORITY_SYSTEM:
├─ PRIMARY SOURCES (최우선)
│  ├─ Original Research Papers (DOI 기반)
│  ├─ Government Official Reports (기관명 + 발행일)
│  ├─ Direct Data Sources (원본 데이터셋)
│  └─ Peer-Reviewed Journals (피어 리뷰 완료)
├─ SECONDARY SOURCES (보조)
│  ├─ Academic Reviews (원본 소스 인용 필수)
│  ├─ Industry Reports (데이터 출처 명시)
│  ├─ Expert Interviews (전문가 자격 검증)
│  └─ Conference Proceedings (학술대회 발표)
└─ TERTIARY SOURCES (제한적)
   ├─ News Articles (원본 소스 연결 필수)
   ├─ Blog Posts (전문가 인용 필수)
   ├─ Social Media (공식 계정만 허용)
   └─ Wikipedia (참고용, 직접 인용 금지)
```

#### 순환참조 탐지 시스템
```circular-reference-detection
CITATION_CHAIN_ANALYZER:
├─ Chain Mapping: A→B→C→A 순환 자동 탐지
├─ Cross-Reference Matrix: 다중 소스 교차 검증
├─ Temporal Consistency: 시간적 일관성 검사
└─ Source Independence: 독립성 검증

DETECTION_RULES:
├─ 순환참조 발견 시: "순환참조 감지됨 - 추가 독립 소스 필요"
├─ 단일 소스 의존 시: "소스 다양성 부족 - 최소 3개 독립 소스 필수"
├─ 시간적 불일치 시: "시간적 일관성 문제 - 시점별 재검증 필요"
└─ 독립성 의심 시: "소스 독립성 의심 - 추가 검증 필요"
```

### 🚫 **Step 1.2: 불확실성 임계점 시스템**

#### 신뢰도 기반 답변 제어
```uncertainty-threshold
CONFIDENCE_MANAGEMENT_PROTOCOL:
├─ < 40% 신뢰도: "현재 증거로는 판단 불가" 강제 출력
├─ 40-60% 신뢰도: "제한적 신뢰도" 경고 표시
├─ 60-80% 신뢰도: "보통 신뢰도" 표준 출력
└─ > 80% 신뢰도: "높은 신뢰도" 신뢰 표시

MANDATORY_OUTPUT_FORMAT:
💡 **핵심 주장**: [신뢰도에 따른 명확한 결론]

🔍 **소스 검증 결과**:
   🟢 강력 (3+ 독립소스, 높은 합의)
   🟡 보통 (2-3 소스, 부분 합의)  
   🔴 약함 (제한적 증거, 추측성)

⚖️ **신뢰도**: [X%] 
   - 소스 품질: [Primary/Secondary/Tertiary 비율]
   - 순환참조: [발견됨/없음]
   - 시간적 유효성: [최신/보통/구형]

🚨 **불확실성 관리**:
   {{ IF 신뢰도 < 40% }}
   ⚠️ **현재 증거로는 판단 불가**: 추가 정보 수집 필요
   
   {{ IF 상충정보 > 50% }}
   ⚠️ **결론 도출 보류**: 상충 정보 해결 필요
   
   {{ IF 정보격차 > 70% }}
   ⚠️ **추가 정보 수집 필요**: [구체적 부족 영역 명시]
```

#### 시간적 유효성 검사
```temporal-validation
TIME_VALIDITY_CHECK:
├─ 6개월 이내: "최신 정보"
├─ 6개월-1년: "보통 정보" 
├─ 1년-2년: "구형 정보" 경고
├─ 2년-5년: "중요한 업데이트 필요" 강력 경고
└─ 5년 이상: "역사적 참고자료" 분류

MANDATORY_TIME_FLAGS:
📅 **정보 시점**: [구체적 발행일/수집일]
⏰ **분석 시점**: [현재 분석 수행 시점]
🔄 **재검토 필요**: [구체적 재검토 시점]
```

### 📊 **Step 1.3: 소스 검증 출력 형식**

#### 강제 출력 구조
```mandatory-output-format
SOURCE_VERIFICATION_OUTPUT:
💎 **핵심 주장**: [신뢰도 기반 명확한 결론]

🔍 **소스 검증 결과**:
   📚 Primary Sources: [개수] (원본 연구/공식 데이터)
   📖 Secondary Sources: [개수] (학술 리뷰/전문가 의견)
   📰 Tertiary Sources: [개수] (보조 참고자료)
   
   🟢/🟡/🔴 **증거 등급**: [구체적 근거와 함께]

⚖️ **신뢰도**: [X%] 
   - 소스 품질: [Primary:Secondary:Tertiary 비율]
   - 순환참조: [발견됨/없음]
   - 시간적 유효성: [최신/보통/구형]
   - 독립성 검증: [통과/의심/실패]

🚨 **불확실성 관리**:
   {{ IF 신뢰도 < 40% }}
   ⚠️ **현재 증거로는 판단 불가**: 
   - 부족한 정보: [구체적 영역]
   - 추가 수집 필요: [구체적 소스 유형]
   
   {{ IF 상충정보 > 50% }}
   ⚠️ **결론 도출 보류**:
   - 상충 내용: [구체적 상충점]
   - 해결 방안: [추가 검증 방법]
   
   {{ IF 정보격차 > 70% }}
   ⚠️ **추가 정보 수집 필요**:
   - 격차 영역: [구체적 부족 영역]
   - 수집 우선순위: [1순위, 2순위, 3순위]

📅 **시간 정보**:
   - 최신 정보: [구체적 날짜]
   - 분석 시점: [현재 시점]
   - 재검토 필요: [구체적 시점]
```

## 🚫 **절대 금지 사항 (소스 검증)**
- ❌ Tertiary 소스만으로 결론 도출
- ❌ 순환참조 무시하고 결론 제시
- ❌ 40% 미만 신뢰도로 확실한 답변
- ❌ 시간적 유효성 무시
- ❌ 소스 독립성 검증 생략

## ⚙️ **시스템 매개변수 (소스 검증)**
```config
source_requirements:
  min_primary: 1 (최소 1개 원본 소스)
  min_total: 3 (최소 3개 총 소스)
  max_tertiary_ratio: 0.3 (최대 30% 보조 소스)
  
confidence_thresholds:
  no_answer: 40% (40% 미만 시 답변 보류)
  warning: 60% (60% 미만 시 경고)
  reliable: 80% (80% 이상 시 신뢰 표시)
  
temporal_flags:
  outdated: 6months (6개월 이상 구형)
  critical: 1year (1년 이상 중요 업데이트 필요)
  historical: 5years (5년 이상 역사적 참고자료)
```

---

### 🎮 **실행 예시: "원자력 에너지의 미래는?"**

```execution
💎 **핵심 주장**: 안전성 개선과 탄소중립 목표로 2040년까지 점진적 확대될 전망 (신뢰도 82%)

🔍 **소스 검증 결과**:
   📚 Primary Sources: 3개 (IAEA World Nuclear Status 2024, MIT Energy Initiative 2023, DOE Nuclear Energy Report 2024)
   📖 Secondary Sources: 2개 (Nature Energy Review 2024, Energy Policy Journal 2024)
   📰 Tertiary Sources: 1개 (World Nuclear News 2024)
   
   🟢 **증거 등급**: 강력 (5개 독립소스, 높은 합의)

⚖️ **신뢰도**: 82%
   - 소스 품질: Primary 50% : Secondary 33% : Tertiary 17%
   - 순환참조: 없음
   - 시간적 유효성: 최신 (모든 소스 2024년)
   - 독립성 검증: 통과

📅 **시간 정보**:
   - 최신 정보: 2024년 8월 기준
   - 분석 시점: 2024년 12월
   - 재검토 필요: 2025년 6월 (6개월 후)

🎯 **실행 지침**:
   - 단기: 소형모듈원전(SMR) 상용화 투자 확대
   - 중기: 사용후핵연료 재처리 기술 개발  
   - 장기: 핵융합 연구 예산 2배 증액

🚨 **위험 관리**:
   주요 리스크: 
   1. 대규모 사고 발생 시 전면 폐기 압력
   2. 핵확산 우려에 따른 규제 강화
   3. 재생에너지 가격 경쟁력 급상승
```

> **시스템 진화**: 강화된 소스 검증을 통한 신뢰도 기반 답변 제어 → 시간적 유효성 보장 → 순환참조 방지로 정보 품질 향상
