# 📚 MakeText: Structured Learning Material Generator

## 🎯 **목적**
정리되지 않은 텍스트를 what_is_ai 폴더와 같은 체계적, 모듈화된 학습 자료로 변환하는 프롬프트 시스템

## 📁 **폴더 구조**

```
prompts/maketext/
├── README.md                           # 이 파일 - 전체 가이드
├── make_textbook.md                    # 메인 프롬프트 - 전체 시스템
├── module_generator.md                 # 서브 프롬프트 - 개별 모듈 생성
├── vocabulary_generator.md             # 서브 프롬프트 - 영어 어휘 가이드 생성
└── quality_checker.md                 # 서브 프롬프트 - 품질 검증
```

## 🚀 **사용법**

### **1. 메인 프롬프트 사용**
```markdown
# make_textbook.md 사용
주제: [주제명]
원본 텍스트: [정리되지 않은 텍스트]
대상 학습자: [초보자/중급자/고급자]
학습 목표: [구체적 학습 목표]
```

### **2. 서브 프롬프트 사용**
```markdown
# module_generator.md 사용
모듈번호: [01-08]
모듈명: [모듈명]
주제: [구체적 주제]
내용: [관련 텍스트]
난이도: [Beginner/Intermediate/Advanced]

# vocabulary_generator.md 사용
주제: [주제명]
기술 용어 목록: [용어들]
난이도: [Beginner to Advanced]
카테고리: [AI/ML, Computer Science, Business]

# quality_checker.md 사용
생성된 학습 자료: [파일들]
검증 기준: [완성도, 일관성, 접근성, 상호 참조]
```

## 📊 **생성되는 구조**

### **파일 구성**
```
[주제명]/
├── 00_README_Index.md                    # 메인 인덱스 및 학습 가이드
├── 01_[기초모듈].md                       # 기초 개념
├── 02_[기술모듈].md                       # 기술 원리
├── 03_[아키텍처모듈].md                   # 아키텍처/구조
├── 04_[프로세스모듈].md                   # 프로세스/과정
├── 05_[이해모듈].md                       # 이해/철학적 관점
├── 06_[능력한계모듈].md                   # 능력과 한계
├── 07_[실용응용모듈].md                   # 실용적 응용
├── 08_[미래방향모듈].md                   # 미래 방향
├── 09_English_Vocabulary_Guide.md         # 영어 어휘 가이드
└── [주제명]_Comprehensive_Guide.md        # 종합 가이드
```

### **모듈 구조**
```markdown
# [번호]. [모듈명]: [부제목]

## Table of Contents
1. [주제 1] (#anchor1)
2. [주제 2] (#anchor2)
3. [주제 3] (#anchor3)

## 1. [주제 1] {#anchor1}
### 정의 및 범위
- 핵심 개념 설명
- 역사적 맥락
- 현재 상태

> #### 📝 **English Vocabulary Support**:
> - **용어 1**: 정의 및 예시
> - **용어 2**: 정의 및 예시

## 2. [주제 2] {#anchor2}
[내용 구조화]
```

## 🎯 **품질 기준**

### **완성도 (95% 이상)**
- 모든 주요 주제 포함
- 체계적 모듈화 완성
- 일관된 포맷팅 적용
- 실용적 예시 충분

### **접근성 (85% 이상)**
- 영어 어휘 지원 완성
- 난이도별 분류 정확
- 학습자 맞춤 경로
- 명확한 설명 품질

### **실용성 (80% 이상)**
- 실제 사용 사례
- 코드 예시 및 기술적 세부사항
- 비즈니스 및 학술적 관점
- 윤리적 고려사항

## 🔄 **처리 단계**

### **Step 1: 텍스트 분석**
1. 원본 텍스트의 주요 주제 추출
2. 개념 간 관계 분석
3. 난이도별 분류
4. 학습 순서 결정

### **Step 2: 모듈 구조 설계**
1. 9개 모듈로 주제 분할
2. 각 모듈의 학습 목표 정의
3. 모듈 간 연결 관계 설정
4. 영어 어휘 목록 추출

### **Step 3: 내용 구조화**
1. 각 모듈의 Table of Contents 생성
2. 섹션별 내용 조직화
3. 영어 어휘 지원 통합
4. 실용적 예시 추가

### **Step 4: 품질 검증**
1. 완성도 검증 (모든 주요 주제 포함)
2. 일관성 검증 (포맷팅, 스타일)
3. 접근성 검증 (난이도별 분류)
4. 상호 참조 검증 (모듈 간 연결)

## 📊 **출력 예시**

### **입력 예시**
```
주제: Machine Learning
원본 텍스트: [정리되지 않은 머신러닝 관련 텍스트]
대상 학습자: 초보자부터 고급자까지
학습 목표: 머신러닝의 기초부터 실무 적용까지 체계적 학습
```

### **출력 예시**
- 00_README_Index.md: 머신러닝 학습 가이드 인덱스
- 01_ML_Fundamentals.md: 머신러닝 기초 개념
- 02_ML_Algorithms.md: 머신러닝 알고리즘
- 03_Neural_Networks.md: 신경망 아키텍처
- 04_ML_Training.md: 훈련 과정
- 05_ML_Understanding.md: 머신러닝 이해
- 06_ML_Capabilities.md: 능력과 한계
- 07_ML_Applications.md: 실용적 응용
- 08_ML_Future.md: 미래 방향
- 09_English_Vocabulary_Guide.md: 영어 어휘 가이드
- Machine_Learning_Comprehensive_Guide.md: 종합 가이드

## 🎯 **특징**

### **1. 모듈화된 학습 경로**
- 9개 독립 모듈로 구성 (01-09)
- 계층적 학습 구조 (기초→기술→응용→미래)
- 난이도별 분류 (🌱 Beginner, 🌿 Intermediate, 🌳 Advanced)

### **2. 영어 어휘 통합**
- 각 모듈에 영어 어휘 지원 섹션 포함
- 포괄적 영어 어휘 가이드 (09번 모듈)
- 발음 가이드 및 사용 예시

### **3. 학습자 중심 설계**
- 다양한 학습 경로 (Fast Track, Comprehensive Path, Academic Path)
- 자기 평가 체크포인트
- 진행 상황 추적 시스템

### **4. 상호 참조 시스템**
- 모듈 간 링크 연결
- 관련 개념 크로스 레퍼런스
- 학습 경로 안내
- 종합 가이드 통합

## 🚀 **시작하기**

1. **make_textbook.md**를 메인 프롬프트로 사용하여 전체 학습 자료 생성
2. **module_generator.md**를 사용하여 개별 모듈 생성 또는 수정
3. **vocabulary_generator.md**를 사용하여 영어 어휘 가이드 생성
4. **quality_checker.md**를 사용하여 생성된 자료의 품질 검증

## 📞 **지원**

이 프롬프트 시스템은 what_is_ai 폴더의 구조화된 텍스트 정리 패턴을 기반으로 설계되었습니다. 

**주요 참조 자료:**
- what_is_ai/00_README_Index.md: 메타 구조 및 학습 가이드
- what_is_ai/01-08 모듈들: 체계적 모듈 구조
- what_is_ai/09_English_Vocabulary_Guide.md: 영어 어휘 가이드

---

**Happy Learning! 🎓**

*이 프롬프트 시스템을 사용하여 정리되지 않은 텍스트를 체계적이고 학습자 친화적인 구조화된 학습 자료로 변환하세요.*
