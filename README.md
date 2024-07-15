# Heart-Failure-Prediction
In this Exploratory Data Analysis (EDA) and a variety of Model Classifications including Logistic Regression (LR), Support Vector Machine (SVM), AdaBoosting (AB), GradientBoosting (GB), K-Nearest Neighbors (KNN), Random Forest (RF), Desicion Tree (DT), XGBoost (XGB), this study will examine the dataset named as "Heart Failure Prediction".
In this study respectively, We have tried to a predict classification problem in Heart Disease Dataset by a variety of models to classifiy Heart Disease predictions in the contex of determining whether anybody is likely to get hearth disease based on the input parameters like gender, age and various test results or not.

This is an extensive analysis of 8 Classification techniques.

# Data
<img width="1003" alt="image" src="https://github.com/Amrapali03/Heart-Failure-Prediction/assets/114306627/e3156752-a7b8-4f92-be94-5d2bfd38f624">



# Contents:


* [   PREFACE](#0)
* [1) LIBRARIES NEEDED IN THE STUDY](#1)

* [2) DATA](#2)

* [3) EXPLORATORY ANALYSIS](#3)
    * [4.1 A General Looking at the Data](#4.1)
    * [4.2 - The Examination of Target Variable](#4.2)
    * [4.3 - The Examination of Numerical Features](#4.3)
    * [4.4 - The Examination of Skewness & Kurtosis](#4.4)
    * [4.5 - The Examination of Numerical Features](#4.5)
    * [4.6 - Dummy Variables Operation](#4.6)    
* [5) TRAIN | TEST SPLIT & HANDLING WITH MISSING VALUES]
* [6) FEATURE SCALLING](#6)
* [7) MODELLING](#7)    
    * [7.1 The Implementation of Logistic Regression (LR)]
    * [7.2 The Implementation of Support Vector Machine (SVM)] 
    * [7.3 The Implementation of Decision Tree (DT)]
    * [7.4 The Implementation of Random Forest (RF)]
    * [7.5 The Implementation of K-Nearest Neighbor (KNN)]
    * [7.6 The Implementation of GradientBoosting (GB)]   
    * [7.7 The Implementation of AdaBoosting (AB)]     
    * [7.8 The Implementation of XGBoosting (XGB)]  
* [8) THE COMPARISON OF MODELS](#8)
* [9) CONLUSION](#9)
* [10) REFERENCES](#10)
* [11) FURTHER READINGS](#11)

## Results: Comparison of Models
![image](https://github.com/Amrapali03/Heart-Failure-Prediction/assets/114306627/826e3cd5-00f8-41db-8e66-5a912ffcd181)


## Steps

We have made the detailed exploratory analysis (EDA).

There have been NO missing values in the Dataset.

We have decided which metrics will be used.

We have analyzed both target and features in detail.

We have transformed categorical variables into dummies so we can use them in the models.

We have handled with skewness problem for make them closer to normal distribution; however, having examined the results, it's clear to assume that handling with skewness could NOT make any contribution to our models when comparing the results obtained by LogisticClassifier without using PowerTransform. Therefore, in this study we have continue not handling with skewness assuming that it's useless for the results.

We have cross-checked the models obtained from train sets by applying cross validation for each model performance.

We have examined the feature importance of some models.

Lastly we have examined the results of all models visually with respect to select the best one for the problem in hand.
