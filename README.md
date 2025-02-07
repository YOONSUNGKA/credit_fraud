# 신용 불이행 예측(25.2.7 기준 데이콘 리더보드 3위_score:0.60998)

## 📌 개요
이 프로젝트는 머신러닝과 딥러닝 기법을 활용하여 신용 불이행 위험을 예측하는 것을 목표로 합니다. 데이터셋에는 다양한 고객 관련 특성이 포함되어 있으며, 모델의 성능은 ROC-AUC 평가 지표를 기준으로 최적화됩니다.

## 📂 프로젝트 구조
```
├── credit_default_17th.ipynb  # 주요 주피터 노트북 파일
├── train.csv                   # 학습 데이터셋
├── test.csv                    # 테스트 데이터셋
├── README.md                   # 프로젝트 문서 (이 파일)
├── requirements.txt            # 필요한 패키지 목록
└── output/                     # 예측 결과 저장 폴더
```

## 🚀 설치 방법
1. 저장소를 클론하거나 노트북 파일을 다운로드합니다.
2. 필요한 라이브러리를 설치합니다:
   ```bash
   pip install -r requirements.txt
   ```

## 📊 방법론
이 노트북은 다음과 같은 순서로 실행됩니다:
1. **데이터 로딩 및 전처리**
   - `train.csv` 및 `test.csv` 불러오기
   - 결측값 처리
   - 범주형 변수 인코딩 (라벨 인코딩 및 원-핫 인코딩 적용)
   - 수치형 변수 로그 변환 적용
   - `StandardScaler`를 사용한 데이터 표준화
   
2. **데이터 불균형 처리**
   - SMOTE (Synthetic Minority Over-sampling Technique) 적용
   
3. **모델 학습**
   - TensorFlow & Keras를 활용한 딥러닝 모델 구현
   - 신경망 아키텍처 정의
   - K-Fold 교차 검증 (10-Fold) 적용하여 학습
   
4. **평가 및 예측**
   - ROC-AUC 점수를 기반으로 모델 평가
   - `test.csv`에 대한 최종 예측 수행

## 📈 모델 성능
- 모델 성능은 ROC-AUC 평가 기준을 따릅니다.
- 데이콘 업로드 결과: 0.60998(25.2.7 기준 3위)

## 🛠 사용 방법
1. `credit_default_17th.ipynb`를 Jupyter Notebook 또는 Google Colab에서 엽니다.
2. 모든 셀을 순차적으로 실행합니다.
3. 최종 예측 파일이 `output/` 폴더에 저장됩니다.

## 📌 향후 개선 사항
- 하이퍼파라미터 최적화 진행
- 다양한 앙상블 기법 적용
- 특성 공학(feature engineering) 기법 탐색을 통한 성능 개선

## 🔗 참고 자료
- [Scikit-learn 공식 문서](https://scikit-learn.org/)
- [TensorFlow/Keras 공식 문서](https://www.tensorflow.org/)

