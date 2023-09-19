# credit-risk-classification
Module 20 Challenge

# Module 20 Report

## Overview of the Analysis
The purpose of this analysis is to evaluate the accuracy of a data model predicting the creditworthiness of borrowers built from historical lending activity. The model was to determine whether a loan to the borrower in the testing set would be low- (0) or high- (1) risk and results are summarized below.

The historical factors decided in the dataset were the size of the loan, interest rate, borrower's income, their debt/income ratio, their number of accounts, negative marks on the borrower, their total debt, and the loan status.

Using 'value_counts' the divide of data points between high- and low- risk loans was clear to see at 2500 to 75036 for a total of 77,536. The dataset was split into training and testing sets using the train_test_split module from scikit-learn. 

The training set was used to build an initial logistic regression model (Logistic Regression Model 1) using the LogisticRegression module from scikit-learn. Logistic Regression Model 1 was then applied to the testing dataset.

To resample the training data and ensure that the logistic regression model had an equal number of data points to draw from, the training set data was resampled with the RandomOverSampler module from imbalanced-learn. This generated 75036 points for each, a total of 150,072. The resampled data was used to build a new logistic regression model (Logistic Regression Model 2). 

## Results

* Machine Learning Model 1:
  * Precision: 93% (an average--in predicting low-risk loans, the model was 100% precise, though the model was only 87% precise in predicting high-risk loans)
  * Accuracy: 95.2%
  * Recall: 95% (an average--the model had 99% recall in predicting low-risk loans, but 91% recall in predicting high-risk loans)


* Machine Learning Model 2:
  * Precision: 99%
  * Accuracy: 99.45%
  * Recall: 99% 

## Summary

Logistic Regression Model 2 is the better suggestion of the two. Less than 0.3% of it's predictions were false positives. It is more important to predict the higher risk loans with more accuracy and this model has a 99.45% balanced accuracy score. 

## References

Data for this dataset was generated by edX Boot Camps LLC, and is intended for educational purposes only.
