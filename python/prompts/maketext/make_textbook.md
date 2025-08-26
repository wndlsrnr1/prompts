# 📚 Make Textbook: Structured Learning Material Generator

## 🎯 **목적**
정리되지 않은 텍스트를 what_is_ai 폴더와 같은 체계적, 모듈화된 학습 자료로 변환하는 프롬프트 시스템

## 📊 **분석된 구조 특징**

### 🏗️ **핵심 구조 패턴**
1. **모듈화된 학습 경로**: 9개 독립 모듈로 구성 (01-09)
2. **계층적 학습 구조**: 기초→기술→응용→미래 순서
3. **영어 어휘 통합**: 각 모듈에 영어 어휘 지원 섹션 포함
4. **다양한 학습 경로**: 초보자/중급자/고급자별 맞춤 경로

### 📁 **파일 구성 패턴**
```
[주제명]/
├── 00_README_Index.md - 메인 인덱스 및 학습 가이드
├── 01_[기초모듈].md - 기초 개념
├── 02_[기술모듈].md - 기술 원리
├── 03_[아키텍처모듈].md - 아키텍처/구조
├── 04_[프로세스모듈].md - 프로세스/과정
├── 05_[이해모듈].md - 이해/철학적 관점
├── 06_[능력한계모듈].md - 능력과 한계
├── 07_[실용응용모듈].md - 실용적 응용
├── 08_[미래방향모듈].md - 미래 방향
├── 09_[어휘가이드].md - 영어 어휘 가이드
└── [주제명]_Comprehensive_Guide.md - 종합 가이드
```

---

## 🚀 **MAIN PROMPT: Structured Textbook Generator**

### **입력 조건**
```
주제: [주제명]
원본 텍스트: [정리되지 않은 텍스트]
대상 학습자: [초보자/중급자/고급자]
학습 목표: [구체적 학습 목표]
```

### **프롬프트 본문**

```
# 📚 [주제명]: Structured Learning Material Generator

당신은 정리되지 않은 텍스트를 체계적이고 학습자 친화적인 구조화된 학습 자료로 변환하는 전문가입니다.

## 🎯 **작업 목표**
주어진 텍스트를 what_is_ai 폴더와 같은 체계적 모듈화된 학습 자료로 변환하여 다음을 생성하세요:

1. **00_README_Index.md**: 메인 인덱스 및 학습 가이드
2. **01-08 모듈들**: 체계적 번호 체계의 학습 모듈들
3. **09_English_Vocabulary_Guide.md**: 영어 어휘 가이드
4. **[주제명]_Comprehensive_Guide.md**: 종합 가이드

## 🏗️ **구조화 원칙**

### **1. 모듈화된 학습 경로**
- **01-03**: 기초 모듈 (🌱 Beginner)
- **04-06**: 중급 모듈 (🌿 Intermediate)  
- **07-08**: 고급 모듈 (🌳 Advanced)
- **09**: 지원 모듈 (📚 Vocabulary Guide)

### **2. 일관된 포맷팅**
- 모든 모듈에 Table of Contents
- 영어 어휘 지원 섹션 통합
- 체계적 번호 체계 (01-09)
- 마크다운 기반 구조화

### **3. 학습자 중심 설계**
- 난이도별 분류 (🌱 Beginner, 🌿 Intermediate, 🌳 Advanced)
- 예상 학습 시간 명시 (30-90분)
- 자기 평가 체크포인트
- 진행 상황 추적

### **4. 상호 참조 시스템**
- 모듈 간 링크 연결
- 관련 개념 크로스 레퍼런스
- 학습 경로 안내
- 종합 가이드 통합

## 📝 **출력 형식**

### **00_README_Index.md 구조**
```markdown
# [주제명]: Comprehensive Guide
**Modular Learning Path with English Vocabulary Support**

## 📚 **Module Overview**
- 학습 경로 시각화
- 난이도별 분류
- 예상 학습 시간
- 핵심 학습 목표

## 🎯 **Learning Path**
```
📖 Module 01: [기초모듈명]
    ↓
🔬 Module 02: [기술모듈명]  
    ↓
⚙️ Module 03: [아키텍처모듈명]
    ↓
🎓 Module 04: [프로세스모듈명]
    ↓
🧠 Module 05: [이해모듈명]
    ↓
⚡ Module 06: [능력한계모듈명]
    ↓
🛠️ Module 07: [실용응용모듈명]
    ↓
🚀 Module 08: [미래방향모듈명]
    ↓
📝 Module 09: English Vocabulary Guide
```

## 📋 **Module Details**
[각 모듈별 상세 설명]

## 🎯 **How to Use This Guide**
[학습자별 가이드]

## 📊 **Learning Progress Tracking**
[진행 상황 추적 시스템]

## 🏆 **Achievement System**
[성취 배지 및 인증 시스템]
```

### **01-08 모듈 구조**
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

## 3. [주제 3] {#anchor3}
[내용 구조화]
```

### **09_English_Vocabulary_Guide.md 구조**
```markdown
# 09. English Vocabulary Guide: Technical Terms and Definitions

## Table of Contents
1. [Introduction to Technical Vocabulary](#introduction)
2. [AI and Machine Learning Terms](#ai-ml-terms)
3. [Computer Science and Technology](#computer-science)
4. [Business and Professional Terms](#business-terms)
5. [Academic and Research Vocabulary](#academic-terms)
6. [Pronunciation Guide](#pronunciation)

## 1. Introduction to Technical Vocabulary {#introduction}
[어휘 가이드 소개]

## 2. AI and Machine Learning Terms {#ai-ml-terms}
### A
**Algorithm** /ˈælɡəˌrɪðəm/
- **Definition**: A step-by-step procedure for solving problems
- **Example**: "The sorting algorithm organizes the data efficiently."
- **Related**: Procedure, method, process
```

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

## 🚀 **실행 지침**

1. **원본 텍스트 분석**: 주제, 구조, 난이도 파악
2. **모듈 설계**: 9개 모듈로 체계적 분할
3. **내용 구조화**: 각 모듈의 체계적 구성
4. **어휘 가이드 생성**: 기술 용어 및 정의
5. **상호 참조 설정**: 모듈 간 연결 및 크로스 레퍼런스
6. **품질 검증**: 완성도, 일관성, 접근성 확인

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

---

**이 프롬프트를 사용하여 정리되지 않은 텍스트를 체계적이고 학습자 친화적인 구조화된 학습 자료로 변환하세요.**
```
