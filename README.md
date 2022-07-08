# Social_Isolation

- 설문지 데이터 분석하기

- 종속변수는 0과 1 사이의 값으로 구성
- 총 1277개 데이터

- 데이터는 비공개 데이터로 깃헙 업로드 불가

- 사용된 알고리즘: Multiple linear regression, SVR, Catboost, Random Forest, DNN
  - 최종모형은 RMSE가 가장 낮은 catboost가 선정되었고,
  - 개인적으로는 DNN이 사용될 것이라고 생각했는데, 생각보다 부스팅 기법(앙상블 기법중 하나)이 성능이 좋아서 놀랐다. 아마도 딥러닝을 돌리기에 충분한 학습 데이터가 아니었나보다. 1277*0.8개의 훈련 데이터.
  - lightGBM과 XGboost도 시도해봤지만, 설문지 데이터라서 그런지, 범주형 catboost
