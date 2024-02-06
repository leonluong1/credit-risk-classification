# Credit Risk Classification Report
Module 20 Supervised Learning Challenge -- Berkeley Data Analytics Boot Camp

## Overview of the Analysis

* The purpose of this analysis is to analyze how well our machine learning model classifies borrowers as healthy or high-risk loans.
* For each borrower, we looked at these features: loan size, interest rate, borrower income, debt-to-income, number of acccounts, derogatory marks and total debt.
* We used the model to predict the loan status of each borrower which the value can either be `0` or `1`.
* The original data includes 75036 healthy loans `0` and 2500 high-risk loans `1`.
* We started off by importing the loan data into a DataFrame and creating a LogisticRegression model.
* Then, we split the data into training and testing sets.
* We fitted the model on the training set and predicted the results on the testing set.
* Next, we created a confusion matrix and classification report to visualize the results.
* Now, we resampled the data to make the loan results more balanced.
* Finally, we fitted a new model based off the oversampled data and repeated the process.

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Balanced Accuracy : 95.2%
  * Precision         : Healthy Loans `0` - 100%  High-risk Loans `1` -  85%
  * Recall Scores     : Healthy Loans `0` -  99%  High-risk Loans `1` -  91%



* Machine Learning Model 2:
  * Balanced Accuracy : 99.4%
  * Precision         : Healthy Loans `0` - 100%  High-risk Loans `1` -  84%
  * Recall Scores     : Healthy Loans `0` -  99%  High-risk Loans `1` -  99%

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

* The oversampled model seems to perform better than the original model in most cases. Both models predict near perfectly for Precision and Recall for the `0` label.
* However, the oversampled model performs better for recall of the `1` label and slightly worse in the precision of the `1` label.
The oversampled model also has a higher balanced accuracy score.

* I recommend the the oversampled model (Model 2) because getting a higher recall score is more important than getting a higher precision score for higher-risk loans.
* Having a lower precision and higher recall score for the `1` label means this model is labeling a few healthy borrowers as "higher-risk". This is more preferrable than labeling higher-risk borrowers as "healthy" because the lending company will lose alot more money on borrowers who cannot pay back than denying a healthy borrower.

