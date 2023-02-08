# Predict student's dropout and academic success

By: Jose Castillo

## Overview

This project aims to identify patterns between student characteristics and academic success. This project will also include a Machine Learning Predictive Model. The dataset includes information about students' marital status, nationality, previous qualification, family background, and more. The Goal is to Predict whether a Student will Dropout or Graduate based on this information.

The dataset can be collected from this page [LINK](https://www.kaggle.com/datasets/thedevastator/higher-education-predictors-of-student-retention)

## Data Understanding

This dataset includes a variety of demographic, social-economic and academic performance data that can be used to predict student dropouts and academic outcomes. Researchers can use this data to answer two key questions:

1.  What specific predictive factors are linked with student dropout or completion?
2.  How do different features interact with each other?

The dataset includes information such as gender, age at enrollment, application mode, marital status, course chosen, curricular units, grades, unemployment rate, inflation rate, and GDP of the region. It is important to note that the dataset is limited to one semester-worth of information for each admission intake and a longer time period might provide more accurate results.

## Exploratory Data Analysis

First We are going to look at a heatmap with our data correlation in order to see there is no multicolliniarity

![image](https://user-images.githubusercontent.com/95591600/217391152-17ca5a5b-07de-4add-8b49-489a0cb2d8c7.png)

Now here is a graph with some of our features with our targets:

![image](https://user-images.githubusercontent.com/95591600/217391242-60630047-0cea-4966-99fe-9b0b26a0d316.png)
![image](https://user-images.githubusercontent.com/95591600/217391380-faf8395c-6cd6-402f-a8f1-0b41e3ec296f.png)
![image](https://user-images.githubusercontent.com/95591600/217392381-165aba0c-99db-4e51-a5d0-64545e37f110.png)

## Data Preparation

The final model for this project will be a Neural Network Model; however, we will be looking and compering different models, that require some pre-processing. Fortunally, there were no missing value in this dataset.

The pre-processing included One Hot Encoder for my categorical values and Standar Scaler for my numerical values. 

## Modeling

For modeling I've tested multiplt ML models including Logistic Regression, Random Forest, K-Nearest Neighbors (KNN), Gradient Boosting, and a Neural Network Model.

For each algorithm, a pipeline was created to preprocess the data and train the classifier. The preprocessor consisted of a ColumnTransformer which applied OneHotEncoding to categorical variables and StandardScaling to numerical variables.

The accuracy of each model was measured using the accuracy_score metric, which compares the predicted labels to the actual labels in the test data. The Logistic Regression model had an accuracy score of 0.759, the Random Forest model had an accuracy score of 0.747, the KNN model had an accuracy score of 0.727, the Gradient Boosting model had an accuracy score of 0.755, and the Neural Network Model was also trained and tested, with an accuracy score of 0.9091. 









