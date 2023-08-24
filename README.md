# Credit Risk Classification

## Overview

The objective of this analysis was to assess the performance of supervised machine learning models using a real-world illustration of loan risk. For this purpose, I employed a logistic regression models to categorize financial data encompassing factors like borrowers' loan size, income, and total debt into either sound or high-risk loan segments. The dataset comprised a total of 77,535 records, out of which 75,036 were designated as healthy loans, while the remaining 2,500 were labeled as high-risk loans.

In order to conduct the analysis, I divided the dataset into two subsets, with 75% allocated for training and the remaining 25% for testing. In the initial trial, I fitted a logistic regression model to the training data and subsequently tested it using the testing data. In the subsequent trial, I rectified the class imbalance in the training data by resampling it, ensuring an equal distribution of 56,277 records within both the healthy and high-risk categories. Then I trained a logistic regression model on the resampled training data and evaluated its performance using the testing data.

## Results

- With the original data, the logistic regression model had an overall accuracy of 99% and a balanced accuracy score of 95%
  - For Healthy loans (0) the model precision is at 100% while the recall is 99% with a 100% f1 score
  - For High-Risk loans (1) predictions, the model precision is 85%, recall is 91% and the f1 score 88%
- For the oversampled data the overall accuracy of the model remains the at 99% however, the balanced accuracy score increased from 95% to 99%
  - For Healthy loans (0) the model precision is at 100% while the recall is 99% with a 100% f1 score
  - For High-Risk loans (1) predictions, the model precision drops to 84%, recall is 99% and the f1 score 91%

## Summary

Overall the second model with the resampled data performed better with a higher balanced accuracy and I would recommend that the company uses that one. The model that used original data had a much higher type 2 error percentage which was drastically decreased in the rebalanced data model. Although the rebalanced data model did have a very slight increase in type 1 error percentage it was only around a .07% increase leading me to believe with the higher balanced accuracy of 99% that the second model with the rebalanced data would be the best choice.
