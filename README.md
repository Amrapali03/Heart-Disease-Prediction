# Heart-Failure-Prediction
In this Exploratory Data Analysis (EDA) and a variety of Model Classifications including Logistic Regression (LR), Support Vector Machine (SVM), AdaBoosting (AB), GradientBoosting (GB), K-Nearest Neighbors (KNN), Random Forest (RF), Desicion Tree (DT), XGBoost (XGB), this study will examine the dataset named as "Heart Failure Prediction" . 

This is an extensive analysis of 8 Classification techniques.

# Contents:
<a id="toc"></a>

<h3 class="list-group-item list-group-item-action active" data-toggle="list" role="tab" aria-controls="home">Table of Contents</h3>

* [   PREFACE](#0)
* [1) LIBRARIES NEEDED IN THE STUDY](#1)
    * [1.1 User Defined Functions](#1.1)
* [2) DATA](#2)
    * [2.1 Context](#2.1)
    * [2.2 About the Features](#2.2)
    * [2.3 What the Problem is](#2.3)
    * [2.4 Target Variable](#2.3)
* [3) ANALYSIS](#3)
    * [3.1) Reading the Data](#3)
* [4) EXPLORATORY DATA ANALYSIS (EDA) & VISUALIZATION](#4)
    * [4.1 A General Looking at the Data](#4.1)
    * [4.2 - The Examination of Target Variable](#4.2)
    * [4.3 - The Examination of Numerical Features](#4.3)
    * [4.4 - The Examination of Skewness & Kurtosis](#4.4)
    * [4.5 - The Examination of Numerical Features](#4.5)
    * [4.6 - Dummy Variables Operation](#4.6)    
* [5) TRAIN | TEST SPLIT & HANDLING WITH MISSING VALUES](#5)    
    * [5.1 Train | Test Split](#5.1)
    * [5.2 Handling with Missing Values](#5.2)
* [6) FEATURE SCALLING](#6)
    * [6.1 The Implementation of Scaling](#6.1)
    * [6.2 General Insights Before Going Further](#6.2)    
    * [6.3 Handling with Skewness with PowerTransform & Checking Model Accuracy Scores](#6.3)
* [7) MODELLING](#7)    
    * [7.1 The Implementation of Logistic Regression (LR)](#7.1)
        * [7.1.a Modelling Logistic Regression (LR) with Default Parameters](#7.1.a)
        * [7.1.b Cross-Validating Logistic Regression (LR) Model](#7.1.b)
        * [7.1.c Modelling Logistic Regression (LR) with Best Parameters Using GridSearchCV](#7.1.c)
        * [7.1.d ROC (Receiver Operating Curve) and AUC (Area Under Curve)](#7.1.d)
        * [7.1.e The Determination of The Optimal Treshold](#7.1.e)
    * [7.2 The Implementation of Support Vector Machine (SVM)](#7.2)
        * [7.2.a Modelling Support Vector Machine (SVM) with Default Parameters](#7.2.a)
        * [7.2.b Cross-Validating Support Vector Machine (SVM)](#7.2.b)
        * [7.2.c Modelling Support Vector Machine (SVM) with Best Parameters Using GridSearchCV](#7.2.c)
        * [7.2.d ROC (Receiver Operating Curve) and AUC (Area Under Curve)](#7.2.d)     
    * [7.3 The Implementation of Decision Tree (DT)](#7.3)
        * [7.3.a Modelling Decision Tree (DT) with Default Parameters](#7.3.a)
        * [7.3.b Cross-Validating Decision Tree (DT)](#7.3.b)
        * [7.3.c Modelling Decision Tree (DT) with Best Parameters Using GridSeachCV](#7.3.c)
        * [7.3.d Feature Importance for Decision Tree (DT) Model](#7.3.d)
        * [7.3.e ROC (Receiver Operating Curve) and AUC (Area Under Curve)](#7.3.e)
        * [7.3.f The Visualization of the Tree](#7.3.f)
    * [7.4 The Implementation of Random Forest (RF)](#7.4)
        * [7.4.a Modelling Random Forest (RF) with Default Parameters](#7.4.a)
        * [7.4.b Cross-Validating Random Forest (RF)](#7.4.b)
        * [7.4.c Modelling Random Forest (RF) with Best Parameters Using GridSeachCV](#7.4.c)
        * [7.4.d Feature Importance for Random Forest (RF) Model](#7.4.d)
        * [7.4.e ROC (Receiver Operating Curve) and AUC (Area Under Curve)](#7.4.e)
        * [7.4.f The Visualization of the Tree](#7.4.f)    
    * [7.5 The Implementation of K-Nearest Neighbor (KNN)](#7.5)
        * [7.5.a Modelling K-Nearest Neighbor (KNN) with Default Parameters](#7.5.a)
        * [7.5.b Cross-Validating K-Nearest Neighbor (KNN)](#7.5.b)
        * [7.5.c Elbow Method for Choosing Reasonable K Values](#7.5.c)
        * [7.5.d GridsearchCV for Choosing Reasonable K Values](#7.5.d)   
        * [7.5.e ROC (Receiver Operating Curve) and AUC (Area Under Curve)](#7.5.e)
    * [7.6 The Implementation of GradientBoosting (GB)](#7.6)
        * [7.6.a Modelling GradientBoosting (GB) with Default Parameters](#7.6.a)
        * [7.6.b Cross-Validating GradientBoosting (GB)](#7.6.b)
        * [7.6.c Feature Importance for GradientBoosting (GB) Model](#7.6.c)
        * [7.6.d Modelling GradientBoosting (GB) with Best Parameters Using GridSearchCV](#7.6.d)        
        * [7.6.e ROC (Receiver Operating Curve) and AUC (Area Under Curve)](#7.6.e)       
    * [7.7 The Implementation of AdaBoosting (AB)](#7.7)
        * [7.7.a Modelling AdaBoosting (AB) with Default Parameters & Model Performance](#7.7.a)
        * [7.7.b Cross-Validating AdaBoosting (AB)](#7.7.b)
        * [7.7.c The Visualization of the Tree](#7.7.c)     
        * [7.7.d Analyzing Performance While Weak Learners Are Added](#7.7.d)         
        * [7.7.e Feature Importance for AdaBoosting (AB) Model](#7.7.e)
        * [7.7.f Modelling AdaBoosting (AB) with Best Parameters Using GridSearchCV](#7.7.f)
        * [7.7.g ROC (Receiver Operating Curve) and AUC (Area Under Curve)](#7.7.g)       
    * [7.8 The Implementation of XGBoosting (XGB)](#7.8)
        * [7.8.a Modelling XGBoosting (XGB) with Default Parameters](#7.8.a)    
        * [7.8.b Cross-Validating XGBoosting (XGB)](#7.8.b)
        * [7.8.c Feature Importance for XGBoosting (XGB) Model](#7.8.c)           
        * [7.8.d Modelling XGBoosting (XGB) with Best Parameters Using GridSearchCV](#7.8.d)     
        * [7.8.e ROC (Receiver Operating Curve) and AUC (Area Under Curve)](#7.8.e)     
* [8) THE COMPARISON OF MODELS](#8)
* [9) CONLUSION](#9)
* [10) REFERENCES](#10)
* [11) FURTHER READINGS](#11)

## Results: Comparison of Models
![image](https://github.com/Amrapali03/Heart-Failure-Prediction/assets/114306627/826e3cd5-00f8-41db-8e66-5a912ffcd181)


## Steps
In this study respectively,

We have tried to a predict classification problem in Heart Disease Dataset by a variety of models to classifiy Heart Disease predictions in the contex of determining whether anybody is likely to get hearth disease based on the input parameters like gender, age and various test results or not.

We have made the detailed exploratory analysis (EDA).

There have been NO missing values in the Dataset.

We have decided which metrics will be used.

We have analyzed both target and features in detail.

We have transformed categorical variables into dummies so we can use them in the models.

We have handled with skewness problem for make them closer to normal distribution; however, having examined the results, it's clear to assume that handling with skewness could NOT make any contribution to our models when comparing the results obtained by LogisticClassifier without using PowerTransform. Therefore, in this study we have continue not handling with skewness assuming that it's useless for the results.

We have cross-checked the models obtained from train sets by applying cross validation for each model performance.

We have examined the feature importance of some models.

Lastly we have examined the results of all models visually with respect to select the best one for the problem in hand.
