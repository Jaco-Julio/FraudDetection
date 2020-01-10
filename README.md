#  Credit Card Fraud Detection kaggle Challenge

Kaggle Project - In order to practice data science and machine learning techniques.

## Description

This challenge aims to build Classifiers capable to identify a credit card transition fraud.  
The dataset contains 30 features and a class with two labels (fraud or non-fraud). PCA has been made for most features and the class is very unbalanced.  
Most features are continuous quantitative. The dataset has 284,806 instances.  

## Exploratory Analysis and creating a good classifier

Exploratory analysis and creation of the best classification model will be described step by step.

1. The dataset from hd was loaded. Because of the file size we could not upload it to github.
2. The labels were visualized and the imbalance was noticed. The label "non-fraud" was 99.83% of the dataset, and the label "fraud" was 0.17% of the dataset. This imbalance may result in overfitting and a bad classifier.
![Imbalance Class](https://github.com/Jaco-Julio/FraudDetection/blob/master/img/imbalance_class.png "Imbalance Class")
3. The dataset was divided into training set and test set.
4. The balance was done with the SMOTE technique. This technique creates synthetic instances at random just like labels. The balance was done in 3 different ways by changing the parameters in SMOTE.
![Balance Class](https://github.com/Jaco-Julio/FraudDetection/blob/master/img/balance1.png "Balance Class")
5. The Logistic Regression, AdaBoosting, Random Forest and K Nearest Neighbors (KNN) algorithms were chosen for classification.
6. The cross_val_score algorithm was used to identify the accuracy of the algorithms in the training sets. It was identified that in the original training set the algorithms ended up generating overfitting.
| **Algorithm** | **Accuracy** |
|:-------------:|:--------:|
| Logistic Regression | 99,89% |
| AdaBoosting | 99,92% |
| Random Forest | 99,95% |
| K Nearest Neighbors (KNN) | 99,83% |
7. The test set was classified and the main metric techniques were used to determine the best classifier. There was also the confusion matrix of the classifiers.

## Analysis of results 

According to the ROC metric, the best classification model was made by the adaboost algorithm.  
| **Algorithm** | **ROC** |
|:-------------:|:--------:|
| Logistic Regression | 91,18% |
| AdaBoosting | 92,04% |
| Random Forest | 89,24% |
| K Nearest Neighbors (KNN) | 68,34% |
but if we analyze from the confusion matrix the best classification model was the random forest algorithm.  
This divergence happens because the difference in the ROC metric between the best score algorithms is 1% or 2%. Therefore, considering the margin of error in the metric in these two algorithms, it can't say which one is the best by the ROC metric. For this, it is necessary to evaluate the confusion matrix, it identifies that the random forest algorithm was more correct.
