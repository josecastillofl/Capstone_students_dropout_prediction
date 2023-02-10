# Predicting student's dropout and academic success

By: Jose Castillo

## Overview

In this project, I aim to explore the factors that influence college student's success and their likelihood of dropping out. By analyzing a dataset that includes information about their background, economic situation, and grades, we aim to gain a better understanding of the factors that affect student retention. The insights gathered from this analysis will be used to make recommendations for the higher education institution to improve student retention and support students in their academic journeys. [DATA](https://www.kaggle.com/datasets/thedevastator/higher-education-predictors-of-student-retention)

![image](https://user-images.githubusercontent.com/95591600/217946329-0ff311b3-5215-4568-91dd-e2a84f0b8bfb.png)

## Busines and Data Understanding

Millions of American college students drop out each year and there are multiple reasons why. The primary reasons are academic struggles and financial concerns. Roughly 25% of first-year college students don't return for their second year to any school and about 35% don't return to the same school. Student debt load has risen steadily over the past two decades and the average debt for 2021 graduates is about $30,000. Schools are trying to keep students in school with initiatives such as scholarships, grants, and emergency grants. Students who struggle in the classroom are also at a high risk of dropping out, so it's important for them to prioritize establishing a strong grade point average early and to meet with academic advisers right away if they begin to struggle. [LINK](https://www.usnews.com/education/best-colleges/articles/2019-03-20/dropping-out-of-college-why-students-do-so-and-how-to-avoid-it)

The dataset I used includes a variety of demographic, social-economic and academic performance data that can be used to predict student dropouts and academic outcomes. Researchers can use this data to answer two key questions:

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

## Modeling

For modeling I've tested multiplt ML models including Logistic Regression, Random Forest, K-Nearest Neighbors (KNN), Gradient Boosting, and a Neural Network Model.

For each algorithm, a pipeline was created to preprocess the data and train the classifier. The preprocessor consisted of a ColumnTransformer which applied OneHotEncoding to categorical variables and StandardScaling to numerical variables.

The accuracy of each model was measured using the accuracy_score metric, which compares the predicted labels to the actual labels in the test data. The Logistic Regression model had an accuracy score of 0.759, the Random Forest model had an accuracy score of 0.747, the KNN model had an accuracy score of 0.727, the Gradient Boosting model had an accuracy score of 0.755, and the Neural Network Model was also trained and tested, with an accuracy score of 0.9091. 









