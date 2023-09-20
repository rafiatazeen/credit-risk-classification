## Overview of the Analysis

The purpose of this analysis was to train and evaluate a machine learning model based on loan risk.  A dataset of historical activity from a peer-to-peer lending services company was used to build this model that can identify the creditworthiness of borrowers. The dataset included information on the loan size, interest rate, borrower income, debt to income, number of accounts, derogatory marks, total debt and loan status which will predict whether a loan can be classified as a healthy loan or a high-risk loan. The variable y was basically the loan status in which 0 was the label for a healthy loan and 1 was the label for a high-risk loan. The rest of the information was under the variable X.

The different stages of the machine learning process that were a part of the anaylsis are:
- load the data and separate the X and y variables
- split the data into training and testing sets
- create and fit a logistic regeression model using the training data
- make predictions for the testing data and generate a confusion matrix
- print the classification report to evaluate how well the model is predicting the healthy loan and high-risk loan
- repeat the steps of creating and fitting a logistic regression model using a resampled dataset that was created to have the same number of data points for both healthy loan and high-risk loan
- make new predictions using resampled dataset and generate another confusion matrix
- print the classification report using the resampled dataset and evaluate how the well the model is predicting both types of loans


## Results

* Machine Learning Model 1:
  - Accuracy - 0.9442676901753825
  - Precision - healthy loan - 1.00, high-risk loan - 0.87
  - Recall - healthy loan - 1.00, high-risk loan - 0.89

* Machine Learning Model 2:
  - Accuracy - 0.9959744975744975
  - Precision - healthy loan - 1.00, high-risk loan - 0.87
  - Recall - healthy loan - 1.00, high-risk loan - 1.00


## Summary
The logistic regression model used with the resampled data seems to perform best. It detects the healthy loan and the high-risk loan correctly 100% of the time with a recall score of 1.00 for both.  The accuracy also improved compared to the first model. The precision scores remained the same for both models with them being able to correctly predict the healthy loans 100% of the time and high-risk loans 87% of the time.  It is more important to predict the '0' correctly than the '1' as it's better for to not take a risk with wrongly predicting a high-risk loan as a healthy loan. I would still recommend using the second model inspite of the precision scores as it is more import of have a higher recall score to ensure that high-risk loans are correctly detected as opposed to if they were wrongly predicted.