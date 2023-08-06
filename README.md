# credit-risk-classification

## Overview of the Analysis

The purpose of this analysis is to build a model that can identify the creditworthiness of borrowers. 

A dataset of historical lending activity from a peer-to-peer lending services company was used to train and evaluate a model based on loan risk. 

To be more precise, the analysis outcome is to determine whether the loan would be "healthy" or "high-risk", based on following parameters (variables):loan size, interest rate,	borrower income, debt to income ratio,	number of accounts,	derogatory marks and total debt.

The analysis had following steps:
* csv file with lending data was imported into jupyter notebook
* data was divided into labels and features
* data was split using train_test_split
* logistic regression model was instantiated, model was fit and prediction made using the testing data
* confusion matrix and classification report were made

## Results

* Machine Learning Model:
  
  * Accuracy - An accuracy of 0.99 indicates that the model is making accurate predictions for the majority of instances.
  * Precision - The model performs exceptionally well for the "Healthy loan" class. It has perfect precision (1.00), meaning that all instances predicted as "Healthy loan"     were actually correct. As for "High-risk loan" class, precision is fairly good. Score of 0.87 means that 87% of the instances predicted as "High-risk loan" were correct.
  * Recall - Recall is perfect for "Healthy loan" class, implying that all actual instances of "Healthy loan" were correctly predicted. As for "High-risk loan" class,         recall score indicates that 89% of all actual instances were correctly predicted.
  * F1-scores of 1.00 and 0.88 respectively also suggest good balance between precision and recall

## Summary

Overall, the logistic regression model demonstrates strong predictive capability for both classes. It correctly identifies the majority of instances for both "Healthy loan" and "High-risk loan," achieving a high level of accuracy. 

However, support values are indicating an imbalanced class distribution which can impact model training and evaluation. In this case, analysis involved 18759 instances of "Healthy loan" class and only 625 instances of "High-risk loan". This could mean that the model hasn't been exposed to as many examples of high-risk loans during training. Therefore, one of the ways to remedy this issue would be to use oversampling for the "High-risk loan" class or undersampling for the "Healthy loan" class. Based on all of this I would recommend this model only in combination with other metrics. 

In addition, in terms of credit risk, it is better to err in the direction of false 1's (false high-risk loans) than in the direction of false 0's (false healthy loans). The goal is to minimize risk of loan default. 

