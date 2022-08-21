# Social_Isolation

- Topic: Predicting social isolation among young people in their 20's
- Period: Apr.01.2022 ~ Jul.02.2022
- data: Korea Institute of Public Administration's Survey on Social Integration in 2021


# Analysis Processes
### 1. Preprocessing
- Data Filtering who are in their 20s  => # of row is 1,277
- Choosing 44 independent variable

### 2. Dependent Variables
- "Social Isolation" was separated into 3 specific isolation: relation isolation, emotional isolation, total isolation
- Selected the 5,3, and 8 questions measuring the 3 different social isolation. -> sum of scored answer.
- Min-Max scaling for comparing the 3 social isolation.


### 3. Modeling
- Linear Regression
- SVR
- Catboost: This is the final model with the lowest test-RMSE.
- Random Forest
- DNN


### 4. Interpreting the Model
- I had known there is hard interpreting for boosting-line models with combined many weak learners.
- So, I tried to interpret the catboost model by applying the SHAP, one of the model-agnostic methods for XAI.


# What I learned
- In my personal opinion, I had thought the DNN methods will record the lowest test-RMSE. In reality, that was not true. I was surprised by the boosting method's performance. Maybe the 1,021 data (1,277\*0.8) was not enough to train the deep learning at backpropagation.
- So, I learned Deep Neural Net is not super in some cases. (Before this project, I had thought DNN is the best method because a more recent method than machine learning.) Furthermore, I thought about the model evaluation metric. If the final model has changed by the used metric in comparing models, What metric will be more persuasive? + Can I say the model superiorness just with the metric? And, Is The model superiorness defined only to predicting and interpreting?
- I explained the XAI concept and implemented the code. I learned the SHAP method based on "Game Theory" and how to calculate the SHAP value.



