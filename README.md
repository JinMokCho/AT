# 📊 BERT Sentiment Analysis Project

## 📖 프로젝트 개요
이 프로젝트는 BERT(Bidirectional Encoder Representations from Transformers) 모델을 사용하여 항공사 트윗의 감정을 분석하는 자연어 처리(NLP) 모델을 구축하는 것입니다. BERT는 양방향 학습을 통해 단어의 의미와 문맥을 이해하는 능력을 갖추고 있습니다.

## 📚 사용된 라이브러리
- **Numpy**: 수치 계산을 위한 라이브러리
- **Pandas**: 데이터 조작 및 분석을 위한 라이브러리
- **Seaborn 및 Matplotlib**: 데이터 시각화를 위한 라이브러리
- **Torch**: 딥러닝 프레임워크
- **Transformers**: BERT 모델과 관련된 라이브러리
- **Datasets**: 데이터셋을 쉽게 로드하고 처리하기 위한 라이브러리

## 📊 데이터셋
- 데이터는 항공사 트윗을 포함하고 있으며, 각 트윗의 감정(긍정, 부정, 중립)과 관련된 메타데이터를 포함합니다.

## 🛠️ 데이터 전처리
- **필요한 열 선택**: 감정과 텍스트 열만 선택하여 새로운 데이터프레임을 생성합니다.
- **감정 레이블 매핑**: 감정 레이블을 숫자(긍정: 1, 부정: 0, 중립: 2)로 매핑하여 새로운 열을 추가합니다.

## 📈 모델 학습 및 평가
- **데이터셋 분할**: 데이터를 학습 세트와 테스트 세트로 나눕니다.
- **BERT 모델 초기화**: DistilBERT 모델을 사용하여 텍스트 분류 작업을 수행합니다.
- **토큰화**: 문장을 토큰화하여 모델에 입력할 수 있는 형태로 변환합니다.
- **훈련 및 평가**: Trainer 클래스를 사용하여 모델을 훈련하고, 정확도 및 F1 점수를 평가합니다.

## 📊 결과
- 모델 훈련 후, 다양한 문장에 대한 감정 예측을 수행할 수 있습니다.

### 예시:
- "I don't like study much" → **negative**
- "I like apple" → **positive**
- "Referees have to stay neutral when making calls in soccer games." → **negative**
