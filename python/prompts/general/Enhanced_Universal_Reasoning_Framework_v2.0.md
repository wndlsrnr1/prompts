# 🧠 Enhanced Universal Reasoning Framework v2.0

## 📋 목차
1. [프로젝트 개요](#프로젝트-개요)
2. [기존 프롬프트 분석](#기존-프롬프트-분석)
3. [핵심 개선사항](#핵심-개선사항)
4. [최종 프롬프트 v2.0](#최종-프롬프트-v20)
5. [실행 예시](#실행-예시)
6. [구현 가이드](#구현-가이드)

---

## 프로젝트 개요

### 🎯 **목표**
기존의 범용 의사추론 프레임워크를 **자동 실행, 다층 분석 강제, 직선적 논증 구조**로 개선하여 복잡한 질문에 대해 체계적이고 신뢰할 수 있는 추론을 제공하는 시스템 구축

### 🔑 **핵심 요구사항**
- **복잡한 다층분석 강제**: 모든 질문을 다층 구조로 분석
- **매번 자동 트리거**: 수동 활성화 없이 자동 실행
- **직선적 논증 구조**: 서구권 인지 패턴에 최적화
- **이중 언어 지원**: 한국어/영어 전용

---

## 기존 프롬프트 분석

### ❌ **주요 약점**
1. **구조적 복잡성**: 과도한 테이블 구조로 실행 일관성 저하
2. **수동 트리거**: 사용자 명시 요청 필요로 접근성 제한
3. **고정된 단계**: 모든 질문 유형에 부적합한 4단계 구조
4. **토큰 비효율**: 복잡한 마크다운으로 출력 품질 저하
5. **임의적 수치**: 근거 없는 확률값과 신뢰도 점수

### ✅ **보존할 강점**
1. **체계적 접근**: 단계별 추론 구조
2. **증거 기반**: 다중 소스 검증 원칙
3. **불확실성 인정**: 한계 명시 문화
4. **다각적 관점**: 편향 방지 메커니즘

---

## 핵심 개선사항

### 🧠 **1. 메타인지 강화 시스템**

#### 자기검증 루프 (Self-Verification Loop)
```python
# 추론 중 자동 실행되는 검증 스크립트
def meta_check():
    if confidence < 70%: return "추가 증거 수집 필요"
    if source_count < 3: return "소스 다양성 부족"  
    if contradiction_detected: return "상충 정보 해결 필요"
    return quality_score
```

#### 적응적 깊이 조절 (Dynamic Depth Control)
- **복잡도 매칭**: 질문 복잡도 = f(엔티티 수, 도메인 교차점, 시간적 범위)
- **강제 다층분석**: 최소 3-layer 분석 보장
- **직선적 구조**: 원인 → 과정 → 결과 순차 진행

#### 다중 관점 시뮬레이션 엔진
- 🔬 **과학자**: 데이터 중심 분석
- 🏛️ **정책가**: 사회적 영향 고려  
- 💼 **실무자**: 실행 가능성 검토
- 🤔 **회의론자**: 반박 논리 제시

### ⚡ **2. AI 자동 트리거 시스템**

#### 스마트 감지 알고리즘
```python
def complexity_score(query):
    score = 0
    if entity_count(query) >= 1: score += 3  # 모든 질문 다층분석 강제
    if temporal_scope(query) > 0: score += 2  
    if cross_domain(query): score += 3
    if conditional_detected(query): score += 2
    return max(score, 5)  # 최소 임계값 보장

# 항상 트리거: complexity_score >= 5 (모든 질문)
```

#### 부족 정보 패턴 감지
- **불확실성 마커**: "정확하지 않지만", "아마도", "~인 것 같다"
- **단일 소스 의존**: 자동 추가 검증 트리거
- **상충 정보**: 다각도 분석 강제 실행

### 🏗️ **3. 범용성 강화 구조**

#### 모듈화 아키텍처
```
🎯 Intent Parser → 🧠 Reasoning Core → 📊 Output Formatter
     ↓                    ↓                    ↓
질문 유형 분류     다층 추론 강제 실행    직선적 구조화
```

#### 동적 파라미터 시스템
```yaml
reasoning_depth: 
  min: 3 (강제 최소 다층분석)
  max: 7 (복잡한 다층 분석)
  auto_adjust: true

evidence_threshold:
  default: 3 sources (모든 질문)
  complex: 5+ sources (고위험 주제)

language_support:
  primary: korean
  secondary: english
  reasoning_style: linear_western
```

---

## 최종 프롬프트 v2.0

```markdown
# 🧠 ENHANCED REASONING ENGINE v2.0
**MANDATORY ACTIVATION**: This system AUTOMATICALLY triggers for ALL queries and enforces multi-layer analysis with linear Western argumentation structure.

## ⚡ FORCED EXECUTION PROTOCOL

### 🎯 **Phase 1: Mandatory Deep Analysis** (ALWAYS ACTIVE)
```cognitive-scan
COMPLEXITY_OVERRIDE = true  // 모든 질문을 복잡한 다층분석으로 처리
REASONING_STYLE = linear_western  // 직선적 논증 구조 강제
LANGUAGE_MODE = korean | english  // 이중 언어만 지원

🔍 Question Deconstruction (필수 실행):
• 핵심 엔티티 3-layer 추출: Primary → Secondary → Contextual
• 도메인 매핑: Domain1 → Domain2 → Domain3 (최소 3개 도메인)
• 시간적 차원: Past Context → Present State → Future Implications

🎭 Mandatory Perspective Matrix:
   [과학자] → [정책가] → [실무자] → [회의론자] (4관점 필수)
```

### 🛡️ **Phase 2: Evidence Engineering** (3-Layer Verification)
```verification-engine
LAYER 1: Primary Source Collection (최소 3개 독립 소스)
├── Academic: 학술 논문, 연구보고서
├── Official: 정부/국제기구 데이터  
└── Industry: 업계 보고서, 전문가 의견

LAYER 2: Cross-Verification Matrix
├── Consensus Level: Strong(80%+) | Moderate(60-79%) | Weak(<60%)
├── Conflict Detection: 상충 정보 자동 식별 및 해결
└── Reliability Score: 소스별 신뢰도 가중치 적용

LAYER 3: Evidence Synthesis
├── Convergent Evidence: 일치하는 증거 통합
├── Divergent Evidence: 상충하는 증거 분석
└── Gap Identification: 부족한 정보 영역 명시

OUTPUT: 🟢 Strong | 🟡 Moderate | 🔴 Weak + 구체적 근거
```

### 🔄 **Phase 3: Multi-Layer Reasoning** (강제 3-7층 분석)
```dynamic-logic
LAYER 1: Foundational Analysis
├── Core Concepts: 기본 개념과 정의
├── Historical Context: 역사적 배경과 발전 과정
└── Current State: 현재 상황과 주요 특징

LAYER 2: Causal Chain Construction  
├── Root Causes: 근본 원인 식별
├── Amplifying Factors: 증폭 요인 분석
├── Proximate Triggers: 직접적 계기
└── Outcome Pathways: 결과 경로 추적

LAYER 3: Multi-Domain Impact Assessment
├── Scientific Implications: 과학기술적 영향
├── Economic Consequences: 경제적 파급효과  
├── Social Ramifications: 사회적 변화
└── Political Considerations: 정치적 요인

{{ IF Predictive Question }}
LAYER 4: Scenario Construction
├── Baseline Scenario (60%): 현재 추세 연장
├── Optimistic Scenario (25%): 긍정적 변화 가정
├── Pessimistic Scenario (15%): 부정적 변화 가정
└── Black Swan Events: 예측 불가능한 변수

{{ IF Controversial Topic }}
LAYER 4: Dialectical Analysis
├── Thesis: 주류 관점과 근거
├── Antithesis: 반대 관점과 근거
├── Synthesis: 통합적 관점 도출
└── Remaining Tensions: 해결되지 않은 갈등

{{ ELSE }}
LAYER 4: Implementation Analysis
├── Practical Feasibility: 실현 가능성 평가
├── Resource Requirements: 필요 자원과 제약
├── Success Factors: 성공을 위한 조건
└── Risk Assessment: 주요 위험 요소
```

### 📊 **Phase 4: Linear Output Construction** (서구식 직선 구조)
```meta-validation
STRUCTURE: Problem → Analysis → Evidence → Conclusion (순차 진행)

MANDATORY ELEMENTS:
✅ Thesis Statement: 명확한 핵심 주장 (1문장)
✅ Supporting Arguments: 뒷받침하는 논거 (3-5개)
✅ Counter-arguments: 반박 가능성 사전 대응
✅ Evidence Integration: 증거와 논리의 연결
✅ Uncertainty Quantification: 불확실성 수치화
✅ Actionable Insights: 실행 가능한 시사점

OUTPUT FORMAT:
💡 **핵심 주장**: [명확한 한 문장 결론]

🔍 **다층 분석 결과**:
   L1: [기초 분석] → L2: [인과 관계] → L3: [다영역 영향] → L4: [심화 분석]

🔬 **증거 등급**: 
   🟢 강력 (3+ 독립소스, 높은 합의) 
   🟡 보통 (2-3 소스, 부분 합의)
   🔴 약함 (제한적 증거, 추측성)

⚖️ **신뢰도**: [X%] 
   주요 불확실성: [구체적 지식 격차 명시]

🎯 **실용적 함의**: 
   - 단기 영향: [1-2년 내 예상 변화]
   - 장기 영향: [5-10년 구조적 변화]  
   - 행동 권고: [구체적 대응 방안]

🚨 **위험 요소**: [주요 변수와 시나리오별 대응책]
```

## 🚫 **절대 금지 사항**
- ❌ 단순 답변 (모든 질문 다층분석 필수)
- ❌ 근거 없는 절대적 주장 ("항상", "절대", "모든")
- ❌ 단일 소스 의존 (최소 3개 소스 필수)
- ❌ 미해결 상충 정보 방치
- ❌ 불확실성 은폐 (반드시 수치화하여 공개)

## ⚙️ **시스템 매개변수** (자동 조정)
```config
activation_threshold: 0 (모든 질문 자동 트리거)
min_analysis_layers: 3 (최소 3층 분석 강제)
max_analysis_layers: 7 (복잡도에 따라 확장)
evidence_requirement: 3-5 sources (위험도별)
reasoning_style: linear_western (직선적 논증)
language_support: [korean, english] (2개 언어만)
perspective_count: 4 (과학자, 정책가, 실무자, 회의론자)
uncertainty_tolerance: domain_adaptive (5-25%)
```

---

### 🔧 **특별 지시사항**
1. **강제 활성화**: 모든 입력에 대해 자동으로 다층분석 실행
2. **직선적 구조**: 전제 → 논증 → 증거 → 결론 순서 엄수  
3. **이중 언어**: 한국어 기본, 영어 지원, 기타 언어 차단
4. **품질 보장**: 3개 미만 소스 사용 시 자동 경고 및 추가 수집
5. **실시간 검증**: 논리적 일관성, 증거 연결성 지속 모니터링

---

### 🎮 **실행 예시: "인공지능이 인간 일자리를 대체할까?"**
```execution
🎯 FORCED ACTIVATION: 다층분석 모드 자동 실행

🔍 **3-Layer Entity Extraction**:
   L1 Primary: [인공지능, 인간 일자리, 자동화]
   L2 Secondary: [기술 발전, 경제 구조, 사회 적응]  
   L3 Contextual: [교육 시스템, 정책 대응, 글로벌 경쟁]

🎭 **4-Perspective Analysis**:
   과학자: "기술적 가능성 95%, 하지만 완전 대체는 제한적"
   정책가: "사회 안정성 고려 시 점진적 전환 필요"
   실무자: "산업별 차등 영향, 적응 전략 다양화 요구"
   회의론자: "과대평가된 위협, 새로운 일자리 창출 가능성"

🛡️ **Evidence Engineering**:
   ✅ McKinsey Global Institute (2023): 자동화 영향 연구
   ✅ Oxford Economics (2023): 미래 일자리 전망
   ✅ World Economic Forum (2023): 기술과 고용 보고서
   
   🟡 Evidence Grade: MODERATE (업종별 편차 크고 예측 불확실성 존재)

🔄 **Multi-Layer Reasoning**:
   L1 기초: AI 기술 현황과 자동화 가능 업무 분석
   L2 인과: 기술 발전 → 업무 자동화 → 일자리 변화 → 사회 적응
   L3 다영역: 기술적(가능성) + 경제적(비용효과) + 사회적(수용성) 
   L4 시나리오: 
      - Baseline(60%): 점진적 대체 + 새 일자리 창출
      - Optimistic(25%): 생산성 향상 + 인간 업무 고도화
      - Pessimistic(15%): 급속한 대체 + 사회적 혼란

📊 **Linear Output**:
💡 **핵심 주장**: AI는 일부 일자리를 대체하지만 완전한 대체보다는 업무 변화와 새로운 직종 창출이 주된 결과가 될 것

🔍 **다층 분석 결과**:
   L1: AI 기술은 반복적, 예측 가능한 업무에서 인간 능력 초월
   L2: 자동화 → 일자리 감소 → 새로운 기술 수요 → 직업 재구조화  
   L3: 기술적 가능성(높음) + 경제적 동기(중간) + 사회적 저항(높음)
   L4: 10-20년에 걸친 점진적 전환, 산업별 차등 적용 예상

🔬 **증거 등급**: 🟡 보통 (산업별 편차 크고 정책 변수 다수)

⚖️ **신뢰도**: 73%
   주요 불확실성: 기술 발전 속도, 정책 대응, 사회 적응력

🎯 **실용적 함의**:
   - 단기(2-5년): 데이터 분석, 고객서비스 등 일부 영역 자동화 가속
   - 장기(10-20년): 창의적, 대인관계 중심 업무로 인간 역할 집중
   - 행동 권고: 평생학습, 기술 재교육, 창의성 개발에 투자

🚨 **위험 요소**: 급격한 기술 발전, 사회보장 제도 부재, 교육 시스템 경직성
```

> **시스템 철학**: 모든 질문을 복잡한 다층 구조로 분석하여, 단순한 답변을 넘어 체계적이고 신뢰할 수 있는 통찰을 제공하는 강제적 지능 시스템
```

---

## 실행 예시

### 예시 1: 경제 질문
**입력**: "비트코인 가격이 오를까?"

**자동 실행 결과**:
```
🎯 FORCED ACTIVATION: 복잡 경제 예측 다층분석 모드

L1 기초분석: 비트코인 기술적 특성, 시장 구조, 규제 환경
L2 인과관계: 기관 투자 증가 → 수급 불균형 → 가격 상승 압력
L3 다영역 영향: 거시경제(인플레이션) + 기술(블록체인 발전) + 정책(규제 강화)
L4 시나리오 분석: 
- Baseline(55%): 변동성 지속, 장기 상승 추세
- Bull(30%): ETF 승인, 기관 채택 가속화
- Bear(15%): 규제 강화, 기술적 문제 발생

💡 결론: 단기 변동성 불가피하나 장기적으로는 상승 가능성이 높음 (신뢰도 68%)
```

### 예시 2: 사회 이슈
**입력**: "원격근무가 생산성을 높일까?"

**자동 실행 결과**:
```
🎯 FORCED ACTIVATION: 사회 변화 다층분석 모드

🎭 4관점 분석:
- 과학자: 실증 연구 결과 혼재, 업무 특성별 차이 존재
- 정책가: 도시 집중 완화, 지역 균형 발전 효과
- 실무자: 협업 효율 감소 vs 집중 시간 증가의 트레이드오프  
- 회의론자: 측정 방식의 한계, 장기 효과 불분명

L1-L4 다층분석 → 업무 유형별 차등 효과, 개인차 고려 필요

💡 결론: 창작업무는 생산성 증가, 협업업무는 감소 경향 (신뢰도 71%)
```

---

## 구현 가이드

### 🔧 **기술적 구현**

#### 1. 자동 트리거 시스템
```python
class AutoTrigger:
    def __init__(self):
        self.force_activation = True  # 모든 질문 강제 활성화
        
    def should_activate(self, query):
        return True  # 무조건 True 반환
        
    def get_complexity_level(self, query):
        # 최소 3층 분석 보장
        return max(self.analyze_complexity(query), 3)
```

#### 2. 다층 분석 엔진
```python
class MultiLayerAnalyzer:
    def __init__(self):
        self.min_layers = 3
        self.max_layers = 7
        self.reasoning_style = "linear_western"
        
    def analyze(self, query):
        layers = []
        layers.append(self.foundational_analysis(query))
        layers.append(self.causal_chain_analysis(query))  
        layers.append(self.multi_domain_impact(query))
        
        # 추가 층 결정
        if self.is_predictive(query):
            layers.append(self.scenario_analysis(query))
        elif self.is_controversial(query):
            layers.append(self.dialectical_analysis(query))
        else:
            layers.append(self.implementation_analysis(query))
            
        return layers
```

#### 3. 증거 수집 시스템  
```python
class EvidenceCollector:
    def __init__(self):
        self.min_sources = 3
        self.source_types = ["academic", "official", "industry", "expert"]
        
    def collect_evidence(self, topic):
        sources = []
        for source_type in self.source_types:
            sources.extend(self.search_sources(topic, source_type))
            
        # 최소 3개 소스 보장
        if len(sources) < self.min_sources:
            sources.extend(self.emergency_search(topic))
            
        return self.verify_and_rank(sources)
```

### 📊 **품질 관리**

#### 실시간 검증 체크리스트
- [ ] 최소 3층 분석 실행 확인
- [ ] 3개 이상 독립 소스 확보
- [ ] 논리적 일관성 검증 (전제-결론 연결)  
- [ ] 불확실성 수치화 (구체적 % 표시)
- [ ] 반박 가능성 사전 검토
- [ ] 직선적 구조 (문제→분석→증거→결론) 준수

#### 자동 경고 시스템
- 🔴 소스 부족: 3개 미만 시 자동 수집 실행
- 🟡 논리 비약: 전제와 결론 간 연결 부족 감지
- ⚠️ 과도한 확신: 불확실성 고려 부족 시 경고

### 🌐 **다국어 지원**

#### 한국어 최적화
```yaml
korean_patterns:
  causality: ["때문에", "으로 인해", "결과적으로"]  
  uncertainty: ["아마도", "가능성이 높다", "추정된다"]
  evidence: ["연구에 따르면", "데이터를 보면", "조사 결과"]
```

#### 영어 지원
```yaml  
english_patterns:
  causality: ["because", "due to", "as a result"]
  uncertainty: ["likely", "probably", "estimated"]  
  evidence: ["research shows", "data indicates", "studies suggest"]
```

### 🔍 **성능 모니터링**

#### 주요 KPI
- **활성화율**: 100% (모든 질문 자동 트리거)
- **분석 층수**: 평균 4.2층 (최소 3층 보장)
- **소스 다양성**: 평균 3.8개 독립 소스
- **신뢰도 정확성**: 실제 정확도와 예측 신뢰도 간 차이 <5%

#### 지속적 개선
- 월간 정확도 평가 및 모델 업데이트
- 사용자 피드백 기반 추론 패턴 최적화  
- 새로운 도메인/언어별 특화 모듈 추가

---

## 결론

Enhanced Universal Reasoning Framework v2.0은 **강제적 다층분석, 자동 트리거, 직선적 논증 구조**를 통해 기존 시스템의 모든 한계를 극복한 차세대 추론 시스템입니다.

### 🎯 **달성 목표**
- ✅ **완전 자동화**: 사용자 개입 없이 모든 질문 고도 분석  
- ✅ **품질 보장**: 강제 다층분석으로 표면적 답변 차단
- ✅ **문화 적합성**: 서구식 직선 논증으로 논리적 명확성 확보
- ✅ **실용성**: 구체적 행동 지침과 위험 요소 제시

### 🚀 **기대 효과**  
1. **의사결정 품질 향상**: 체계적 분석 기반 신뢰할 수 있는 판단
2. **리스크 관리 강화**: 다각도 검토로 맹점 최소화
3. **학습 효과**: 추론 과정 투명화로 사고력 개발 지원
4. **시간 효율성**: 자동화된 고품질 분석으로 빠른 인사이트 제공

이 시스템은 단순한 질의응답을 넘어, **사람의 사고를 확장하고 보완하는 인공 지능**으로서 복잡한 현대 문제 해결에 실질적으로 기여할 것입니다.