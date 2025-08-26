# 📝 MakeText 프롬프트 사용 예시: Machine Learning 주제

## 🎯 **목적**
Machine Learning 주제를 예시로 하여 MakeText 프롬프트 시스템의 실제 사용 과정을 단계별로 보여줌

---

## 🚀 **1단계: 메인 프롬프트 실행**

### **1.1 입력 준비**
```markdown
주제: Machine Learning
원본 텍스트: 
머신러닝은 인공지능의 한 분야로, 컴퓨터가 데이터로부터 학습하여 패턴을 발견하고 예측을 수행하는 기술입니다. 머신러닝은 지도학습, 비지도학습, 강화학습으로 나뉩니다. 지도학습은 레이블이 있는 데이터로 학습하는 방식이고, 비지도학습은 레이블이 없는 데이터에서 패턴을 찾는 방식입니다. 강화학습은 환경과의 상호작용을 통해 학습하는 방식입니다.

주요 알고리즘으로는 선형회귀, 로지스틱회귀, 결정트리, 랜덤포레스트, SVM, 신경망 등이 있습니다. 선형회귀는 연속적인 값을 예측하는 데 사용되고, 로지스틱회귀는 분류 문제에 사용됩니다. 결정트리는 if-then 규칙을 기반으로 한 알고리즘이고, 랜덤포레스트는 여러 결정트리를 조합한 앙상블 방법입니다.

신경망은 인간의 뇌를 모방한 알고리즘으로, 여러 층의 뉴런으로 구성됩니다. 딥러닝은 여러 층의 신경망을 사용하는 머신러닝의 한 분야입니다. CNN은 이미지 처리에 특화된 신경망이고, RNN은 순차 데이터 처리에 특화된 신경망입니다.

머신러닝의 성능 평가는 정확도, 정밀도, 재현율, F1-score 등으로 측정됩니다. 과적합과 과소적합은 머신러닝에서 자주 발생하는 문제입니다. 과적합은 훈련 데이터에 너무 맞춰져서 일반화 성능이 떨어지는 현상이고, 과소적합은 모델이 너무 단순해서 훈련 데이터도 잘 맞추지 못하는 현상입니다.

머신러닝은 이미지 인식, 자연어 처리, 추천 시스템, 자율주행차, 의료 진단 등 다양한 분야에서 활용되고 있습니다. 향후에는 더욱 정교한 알고리즘과 대규모 데이터를 활용한 발전이 예상됩니다.

대상 학습자: 초보자부터 고급자까지
학습 목표: 머신러닝의 기초부터 실무 적용까지 체계적 학습
```

### **1.2 메인 프롬프트 실행**
```markdown
# 📚 Machine Learning: Structured Learning Material Generator

당신은 정리되지 않은 텍스트를 체계적이고 학습자 친화적인 구조화된 학습 자료로 변환하는 전문가입니다.

## 🎯 **작업 목표**
주어진 텍스트를 what_is_ai 폴더와 같은 체계적 모듈화된 학습 자료로 변환하여 다음을 생성하세요:

1. **00_README_Index.md**: 메인 인덱스 및 학습 가이드
2. **01-08 모듈들**: 체계적 번호 체계의 학습 모듈들
3. **09_English_Vocabulary_Guide.md**: 영어 어휘 가이드
4. **Machine_Learning_Comprehensive_Guide.md**: 종합 가이드

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

[위의 원본 텍스트를 여기에 붙여넣기]
```

### **1.3 1단계 출력물 예시**
```markdown
# 00_README_Index.md 생성
# Machine Learning: Comprehensive Guide
**Modular Learning Path with English Vocabulary Support**

## 📚 **Module Overview**
- 학습 경로 시각화
- 난이도별 분류
- 예상 학습 시간
- 핵심 학습 목표

## 🎯 **Learning Path**
```
📖 Module 01: ML Fundamentals
    ↓
🔬 Module 02: ML Algorithms  
    ↓
⚙️ Module 03: Neural Networks
    ↓
🎓 Module 04: Training Processes
    ↓
🧠 Module 05: ML Understanding
    ↓
⚡ Module 06: ML Capabilities & Limitations
    ↓
🛠️ Module 07: Practical Applications
    ↓
🚀 Module 08: Future Directions
    ↓
📝 Module 09: English Vocabulary Guide
```

# 01_ML_Fundamentals.md 생성
# 01. ML Fundamentals: Introduction to Machine Learning

## Table of Contents
1. [What is Machine Learning?](#what-is-ml)
2. [Types of Machine Learning](#types-of-ml)
3. [Key Concepts and Terminology](#key-concepts)

## 1. What is Machine Learning? {#what-is-ml}
### 정의 및 범위
Machine Learning은 인공지능의 한 분야로, 컴퓨터가 데이터로부터 학습하여 패턴을 발견하고 예측을 수행하는 기술입니다.

> #### 📝 **English Vocabulary Support**:
> - **Machine Learning**: A subset of AI that enables systems to learn from data
> - **Pattern**: Regular, repeated arrangements or sequences
> - **Prediction**: Using data to forecast future events or trends
```

---

## 🔧 **2단계: 서브 프롬프트 실행**

### **2.1 모듈 생성 (module_generator.md)**

#### **2.1.1 01번 모듈 생성**
```markdown
# 🔧 Module Generator: 01 ML Fundamentals

당신은 특정 주제를 체계적이고 학습자 친화적인 모듈로 구조화하는 전문가입니다.

## 🎯 **작업 목표**
주어진 주제와 내용을 what_is_ai 폴더의 모듈 구조에 맞춰 체계적으로 구성하여 다음을 생성하세요:

1. **Table of Contents**: 명확한 목차 구조
2. **체계적 섹션 구성**: 논리적 순서의 섹션들
3. **영어 어휘 지원**: 통합된 어휘 가이드
4. **실용적 예시**: 실제 사용 사례 및 코드 예시

## 📝 **입력 정보**
모듈번호: 01
모듈명: ML Fundamentals
주제: 머신러닝의 기본 개념과 정의
내용: 머신러닝은 인공지능의 한 분야로, 컴퓨터가 데이터로부터 학습하여 패턴을 발견하고 예측을 수행하는 기술입니다. 머신러닝은 지도학습, 비지도학습, 강화학습으로 나뉩니다.
난이도: Beginner

[ML 기초 관련 텍스트를 여기에 붙여넣기]
```

#### **2.1.2 02번 모듈 생성**
```markdown
# 🔧 Module Generator: 02 ML Algorithms

당신은 특정 주제를 체계적이고 학습자 친화적인 모듈로 구조화하는 전문가입니다.

## 🎯 **작업 목표**
주어진 주제와 내용을 what_is_ai 폴더의 모듈 구조에 맞춰 체계적으로 구성하여 다음을 생성하세요:

1. **Table of Contents**: 명확한 목차 구조
2. **체계적 섹션 구성**: 논리적 순서의 섹션들
3. **영어 어휘 지원**: 통합된 어휘 가이드
4. **실용적 예시**: 실제 사용 사례 및 코드 예시

## 📝 **입력 정보**
모듈번호: 02
모듈명: ML Algorithms
주제: 주요 머신러닝 알고리즘
내용: 주요 알고리즘으로는 선형회귀, 로지스틱회귀, 결정트리, 랜덤포레스트, SVM, 신경망 등이 있습니다.
난이도: Intermediate

[ML 알고리즘 관련 텍스트를 여기에 붙여넣기]
```

### **2.2 어휘 가이드 생성 (vocabulary_generator.md)**

#### **2.2.1 어휘 가이드 생성**
```markdown
# 📚 Vocabulary Generator: English Vocabulary Guide

당신은 기술 용어와 개념에 대한 체계적이고 포괄적인 영어 어휘 가이드를 생성하는 전문가입니다.

## 🎯 **작업 목표**
주어진 주제와 관련된 기술 용어들을 분석하여 what_is_ai 폴더의 09_English_Vocabulary_Guide.md와 같은 구조의 어휘 가이드를 생성하세요:

1. **알파벳순 구성**: A-Z 순서로 용어 정리
2. **발음 가이드**: IPA 발음 기호 포함
3. **정의 및 예시**: 명확한 정의와 사용 예시
4. **관련 용어**: 연결된 개념과 동의어

## 📝 **입력 정보**
주제: Machine Learning
기술 용어 목록: Machine Learning, Supervised Learning, Unsupervised Learning, Reinforcement Learning, Linear Regression, Logistic Regression, Decision Tree, Random Forest, SVM, Neural Network, Deep Learning, CNN, RNN, Overfitting, Underfitting, Accuracy, Precision, Recall, F1-score
난이도: Beginner to Advanced
카테고리: AI/ML, Computer Science, Statistics

[기술 용어 목록을 여기에 붙여넣기]
```

### **2.3 2단계 출력물 예시**
```markdown
# 완성된 01_ML_Fundamentals.md
# 01. ML Fundamentals: Introduction to Machine Learning

## Table of Contents
1. [What is Machine Learning?](#what-is-ml)
2. [Types of Machine Learning](#types-of-ml)
3. [Key Concepts and Terminology](#key-concepts)

## 1. What is Machine Learning? {#what-is-ml}
### 정의 및 범위
Machine Learning은 인공지능의 한 분야로, 컴퓨터가 데이터로부터 학습하여 패턴을 발견하고 예측을 수행하는 기술입니다.

> #### 📝 **English Vocabulary Support**:
> - **Machine Learning**: A subset of AI that enables systems to learn from data
> - **Pattern**: Regular, repeated arrangements or sequences
> - **Prediction**: Using data to forecast future events or trends

### 핵심 특징
- 데이터 기반 학습
- 패턴 발견 및 예측
- 자동화된 의사결정
- 지속적 성능 향상

## 2. Types of Machine Learning {#types-of-ml}
### 지도학습 (Supervised Learning)
지도학습은 레이블이 있는 데이터로 학습하는 방식입니다.

> #### 📝 **English Vocabulary Support**:
> - **Supervised Learning**: Learning with labeled training data
> - **Label**: The correct answer or target value for training data
> - **Training Data**: Data used to teach the model

### 비지도학습 (Unsupervised Learning)
비지도학습은 레이블이 없는 데이터에서 패턴을 찾는 방식입니다.

> #### 📝 **English Vocabulary Support**:
> - **Unsupervised Learning**: Learning without labeled training data
> - **Pattern Discovery**: Finding hidden patterns in data
> - **Clustering**: Grouping similar data points together
```

---

## ✅ **3단계: 품질 검증**

### **3.1 품질 검증 실행 (quality_checker.md)**

#### **3.1.1 품질 검증 프롬프트**
```markdown
# ✅ Quality Checker: Structured Learning Material Verification

당신은 구조화된 학습 자료의 품질을 체계적으로 검증하는 전문가입니다.

## 🎯 **검증 목표**
생성된 학습 자료가 what_is_ai 폴더의 품질 기준을 충족하는지 확인하여 다음을 검증하세요:

1. **완성도 검증**: 모든 주요 주제 포함 여부
2. **일관성 검증**: 포맷팅, 스타일, 구조의 일관성
3. **접근성 검증**: 학습자 친화적 설계
4. **상호 참조 검증**: 모듈 간 연결 및 크로스 레퍼런스

## 📝 **검증 대상**
생성된 학습 자료: 
- 00_README_Index.md
- 01_ML_Fundamentals.md
- 02_ML_Algorithms.md
- 03_Neural_Networks.md
- 04_ML_Training.md
- 05_ML_Understanding.md
- 06_ML_Capabilities.md
- 07_ML_Applications.md
- 08_ML_Future.md
- 09_English_Vocabulary_Guide.md
- Machine_Learning_Comprehensive_Guide.md

검증 기준: 완성도, 일관성, 접근성, 상호 참조

[생성된 파일들을 여기에 붙여넣기]
```

### **3.2 품질 검증 결과 예시**
```markdown
📊 **품질 검증 결과**
- 완성도: 38/40점 (95%)
- 일관성: 27/30점 (90%)
- 접근성: 18/20점 (90%)
- 상호 참조: 9/10점 (90%)
- **총점: 92/100점 (92%)**
- **등급: 우수**

🔧 **개선 사항**
1. 03_Neural_Networks.md의 코드 예시 추가 필요
2. 07_ML_Applications.md의 실제 사례 보강 필요
3. 모듈 간 크로스 레퍼런스 연결 강화 필요

💡 **권장 사항**
1. 신경망 관련 실제 구현 예시 추가
2. 실무 적용 사례 구체화
3. 모듈 간 연결 링크 보강
```

---

## 🎯 **4단계: 최종 산출물**

### **4.1 최종 파일 구조**
```
Machine_Learning/
├── 00_README_Index.md                    # 메인 인덱스 및 학습 가이드
├── 01_ML_Fundamentals.md                 # 머신러닝 기초 개념
├── 02_ML_Algorithms.md                   # 머신러닝 알고리즘
├── 03_Neural_Networks.md                 # 신경망 아키텍처
├── 04_ML_Training.md                     # 훈련 과정
├── 05_ML_Understanding.md                # 머신러닝 이해
├── 06_ML_Capabilities.md                 # 능력과 한계
├── 07_ML_Applications.md                 # 실용적 응용
├── 08_ML_Future.md                       # 미래 방향
├── 09_English_Vocabulary_Guide.md        # 영어 어휘 가이드
└── Machine_Learning_Comprehensive_Guide.md # 종합 가이드
```

### **4.2 최종 산출물 특징**
- ✅ 체계적 모듈화 (9개 모듈)
- ✅ 영어 어휘 지원 통합
- ✅ 학습자 중심 설계
- ✅ 상호 참조 시스템
- ✅ 품질 검증 완료 (92점/100점)

---

## 🎯 **성공 팁**

### **1. 입력 준비**
- 원본 텍스트를 충분히 제공 (최소 500자 이상)
- 구체적인 주제와 학습 목표 설정
- 대상 학습자 명확히 정의

### **2. 단계별 실행**
- 1단계 완료 후 2단계 진행
- 각 단계의 출력물 검토
- 필요시 반복 실행

### **3. 품질 관리**
- 품질 검증 결과 확인
- 개선 사항 반영
- 최종 검증 완료

### **4. 지속적 개선**
- 사용자 피드백 수집
- 프롬프트 개선
- 새로운 주제 적용

---

**이 예시를 참고하여 다른 주제에 대해서도 동일한 과정을 따라 체계적이고 학습자 친화적인 구조화된 학습 자료를 생성할 수 있습니다.**
