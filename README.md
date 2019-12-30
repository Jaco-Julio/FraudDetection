#  Credit Card Fraud Detection kaggle Challenge

Kaggle Project - In order to practice data science and machine learning techniques.

## Description

This challenge aims to build classifiers/Regressors capable of identifying credit card transition fraud.  
The dataset contains 30 attributes and a class with two labels (fraud or non-fraud). PCA has been made for most attributes and the class is very unbalanced.  
Most attributes are continuous quantitative. The dataset has 284,806 instances.  

## Exploratory Analysis and creating a good classifier

Exploratory analysis and creation of the best classification model will be described step by step.

1. The dataset from hd was loaded. Because of the file size we could not upload it to github.
2. The labels were visualized and the imbalance was noticed. The label "non-fraud" was 9.83% of the dataset, and the label "fraud" was 0.17% of the dataset. This imbalance may result in overfitting.
3. The dataset was divided into training set and test set.
4. The balance was done with the SMOTE technique. This technique creates synthetic instances at random just like labels. The balance was done in 3 different ways by changing the parameters in SMOTE.
5. The Logistic Regression, AdaBoosting, Random Forest and K Nearest Neighbors (KNN) algorithms were chosen for classification.
6. The cross_val_score algorithm was used to identify the accuracy of the algorithms in the training sets. It was identified that in the original training set the algorithms ended up generating overfitting.
7. The test set was classified and the main metric techniques were used to determine the best classifier. There was also the confusion matrix of the classifiers.

## Analysis of results 
