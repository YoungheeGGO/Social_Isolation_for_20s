# Social_Isolation

- Topic: Predicting social isolation among young people in their 20's
- Period: Apr.01.2022 ~ Jul.02.2022
- data: Korea Institute of Public Administration's Survey on Social Integration in 2021


# Analysis Processes
### 1. Preprocessing
- Data Filtering who are in their 20s  -> # of row is 1,277
- Choosing 44 independent variable

### 2. Dependent Variables
- "Social Isolation" was separated into 3 specific isolation: relation isolation, emotional isolation, total isolation
- Selected the 5,3, and 8 questions measuring the 3 different social isolation. -> sum of scored answer.
- Min-Max scaling for comparing the 3 social isolation.


### 3. Modeling
- Linear Regression
- SVR
- Catboost
- Random Forest
- DNN
</br>

- The final model is Catboost with the lowest test-RMSE.

### 4. Interpreting the Model
- I had known there is hard interpreting for boosting-line models with combined many weak learners.
- So, I tried to interpret the catboost model by applying the SHAP, one of the model-agnostic methods for XAI.


# What I learned
- In my personal opinion, I had thought the DNN methods will record the lowest test-RMSE. In reality, that was not true. I was surprised by the boosting method's performance. Maybe the 1,021 data (1,277\*0.8) was not enough to train the deep learning at backpropagation.
- So, I learned Deep Neural Net is not super in some cases. (Before this project, I had thought DNN is the best method because a more recent method than machine learning.) Furthermore, I thought about the model evaluation metric. If the final model has changed by the used metric in comparing models, What metric will be more persuasive? + Can I say the model superiorness just with the metric? And, Is The model superiorness defined only to predicting and interpreting?
- 



- XAI 개념들을 직접 구현해보면서 직접 설명을 해보았다. 게임이론을 기반으로 하는 SHAP 기법에 대한 이론적 기반을 공부하였고, 어떠한 원리로 SHAP vlaue가 계산되는지를 배웠다.


- 마지막으로 제일 중요한 리더십을 배울 수 있었다. 원래는 나(팀장) 포함 3명이 팀으로 진행되었지만, 한 명이 매우 비협조적인 태도로 본인 할당량을 해오지 않거나, 매우 뺀질(?) 거렸다. 그래서 다른 팀원과 내가 개인 할당량 이상의 것을 해내야하는 상황이었고, 비협조적인 팀원이 본인의 일을 3번 정도 해오지 않자, 나는 그냥 그 팀원의 이름을 빼버렸다. 아무리 이야기를 해도 팀원은 변화되는 모습을 보여주지 않았다. 다행히도, 팀원 변경이 가능했다! 하지만 팀원 변경을 할 수 없을때, 이러한 팀원을 어떻게 데리고 가야할 지는 잘 모르겠다. 그냥 운이 나빴다고 생각하며 팀원이 변경될 때 까지 다른 팀원과 내가 주어진 일 이상의 것을 해야하는 거겠지...? 하지만 팀 단위로 성과를 내는 것이기 때문에, 일은 다른 사람들이 다 했는데 하나도 하지 않고 팀 내 성과를 홀라당 가져가는 것도 너무 너무 싫을 것 같다. 그냥 이런 팀원을 더 이상 만나지 않길 바란다. 여태 나랑 같이 프로젝트를 했던 친구들이 새삼 고마웠다. 다들 열심히 해주었기 때문에 그동안의 프로젝트에서는 팀 내부의 이슈가 없었는데, 이번 프로젝트에서 처음으로 이러한 상황을 접해보고 나름의 대처를 해보았다. 다음에도 이러한 상황이 생기면 더 현명하게 대처해봐야지.



