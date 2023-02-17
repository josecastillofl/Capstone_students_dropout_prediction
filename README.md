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

![image](https://user-images.githubusercontent.com/95591600/219779378-62513a5c-1ef3-4e75-9010-4e442785e14d.png)
![image](https://user-images.githubusercontent.com/95591600/219779542-cb94b3fb-9b86-4fdf-afc4-3a3a1f9a9c7f.png)
![image](https://user-images.githubusercontent.com/95591600/219779263-ebdbeb24-49fb-44a0-a7dc-855334dcb1b9.png)
![image](https://user-images.githubusercontent.com/95591600/219779715-50361ef6-a30e-451c-bd30-8e335e10c061.png)

## Modeling

For modeling I've tested multiplt ML models including Logistic Regression, Random Forest, K-Nearest Neighbors (KNN), Gradient Boosting, and a Neural Network Model.

For each algorithm, a pipeline was created to preprocess the data and train the classifier. The preprocessor consisted of a ColumnTransformer which applied OneHotEncoding to categorical variables and StandardScaling to numerical variables.

The accuracy of each model was measured using the accuracy_score metric, which compares the predicted labels to the actual labels in the test data. For my baseline model, I used a majority classifier with an accuracy score of 60.8%, the Logistic Regression model had an accuracy score of 75.9%, the Random Forest model had an accuracy score of 74.7%, the KNN model had an accuracy score of 72.7%, the Gradient Boosting model had an accuracy score of 75.5%.

Lastly, I decided to used a Neural Network Model using TensorFlow's Keras library. The model is a simple feedforward Neural Network, consisting of three dense layers. The first layer has 10 units, the second layer also has 10 units, and the final layer has 1 unit. ReLU activation is used in the first two layers and a sigmoid activation is used in the final layer. The model is compiled with the Adam optimizer and the binary cross-entropy loss function, and I ended up with an accuracy score of 91.3%.

## Conclusion

- Using the Neural Network  Predictive Model, we can get an early intervention with student who are likely to dropout, and have a more personalized support for them.

- Promoting scholarships, and make it easy for students to apply, since scholarship holders are 10x more likely to graduate.

## Repo Navigation

Here is the [Main Notebook](/Index.ipynb)
The notebook containing the Graphs [EDA](/EDA.ipynb)



