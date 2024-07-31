# Heart-Failure-Prediction
This study aims to predict the accuracy of demographic and clinical factors leading to heart disease using various machine-learning models. Conducted a thorough exploratory analysis including skewness and kurtosis, dummy encoding of categorical variables, feature scaling, cross-validations, feature importance, and validated the evaluation metrics. Visual comparisons of model results guided selection for optimal heart disease prediction with the GradientBoosting model providing an accuracy of 91.9%.

In this Exploratory Data Analysis (EDA) and a variety of Model Classifications including Logistic Regression (LR), Support Vector Machine (SVM), AdaBoosting (AB), GradientBoosting (GB), K-Nearest Neighbors (KNN), Random Forest (RF), Decision Tree (DT), XGBoost (XGB), this study will examine the dataset named as "Heart Failure Prediction".
In this study respectively, We have tried to a predict classification problem in the Heart Disease Dataset by a variety of models to classify Heart Disease predictions in the context of determining whether anybody is likely to get heart disease based on input parameters like gender, age, and various test results or not.

This is an extensive analysis of 8 Classification techniques.



# Contents of Python File:

1. LIBRARIES NEEDED IN THE STUDY

2. DATA
<img width="1003" alt="image" src="https://github.com/Amrapali03/Heart-Failure-Prediction/assets/114306627/e3156752-a7b8-4f92-be94-5d2bfd38f624">

<img width="410" alt="image" src="https://github.com/user-attachments/assets/92cfbb14-50bc-4b2d-8ce6-e549a31a679b">


3. EXPLORATORY ANALYSIS
    - 3.1 A General Look at the Data
    - 3.2 The Examination of Target Variable
    - 3.3 The Examination of Numerical Features
    - 3.4 The Examination of Skewness & Kurtosis
    - 3.5 The Examination of Numerical Features
    - 3.6 Dummy Variables Operation

![image](https://github.com/user-attachments/assets/eb53ba0b-ca81-41a1-b225-deeb576655dc)



4. TRAIN | TEST SPLIT & HANDLING WITH MISSING VALUES

5. FEATURE SCALING

6. MODELLING
    - 6.1 The Implementation of Logistic Regression (LR)
    - 6.2 The Implementation of Support Vector Machine (SVM)
    - 6.3 The Implementation of Decision Tree (DT)
    - 6.4 The Implementation of Random Forest (RF)
    - 6.5 The Implementation of K-Nearest Neighbor (KNN)
    - 6.6 The Implementation of Gradient Boosting (GB)
    - 6.7 The Implementation of AdaBoosting (AB)
    - 6.8 The Implementation of XGBoosting (XGB)

7. THE COMPARISON OF MODELS
![image](https://github.com/user-attachments/assets/20dde950-15f8-462a-89f8-1a1de04af9db)


8. Conclusion

We have made the detailed exploratory analysis (EDA). There have been NO missing values in the Dataset. We have decided which metrics will be used. We have analyzed both target and features in detail. We have transformed categorical variables into dummies so we can use them in the models.

We have handled with skewness problem for make them closer to normal distribution; however, having examined the results, it's clear to assume that handling with skewness could NOT make any contribution to our models when comparing the results obtained by LogisticClassifier without using PowerTransform. Therefore, in this study we have continue not handling with skewness assuming that it's useless for the results.

We have cross-checked the models obtained from train sets by applying cross validation for each model performance. We have examined the feature importance of some models.

Lastly we have examined the results of all models visually with respect to select the best one for the problem in hand.
