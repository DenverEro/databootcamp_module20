# Module 20 Report: Credit Risk Analysis

## Overview of the Analysis

In this analysis, I built a machine learning model to assess credit risk for a peer-to-peer lending company. The purpose was to develop a model that could accurately identify the creditworthiness of borrowers.

* The financial data analyzed included information about loans such as loan size, interest rate, borrower income, debt-to-income ratio, number of accounts, derogatory marks, and total debt.
* The target variable I needed to predict was the 'loan_status', where 0 represented a healthy loan and 1 represented a high-risk loan with high probability of defaulting.
* The dataset contained 77,536 records with an imbalanced distribution: the majority were healthy loans (0) with a smaller portion being high-risk loans (1).
* The machine learning process involved:
  1. Reading and preprocessing the lending data
  2. Separating the features (X) from the target variable (y)
  3. Splitting the data into training and testing sets using train_test_split
  4. Training a LogisticRegression model on the training data
  5. Making predictions on the test data
  6. Evaluating the model's performance using confusion matrix and classification report

* The primary algorithm used was Logistic Regression, which is appropriate for binary classification problems such as this one.

## Results

* Machine Learning Model: Logistic Regression
  * Accuracy: 99% - The model correctly classified 99% of all loans
  * Precision:
    * Healthy Loans (0): 100% - When the model predicted a loan as healthy, it was correct 100% of the time
    * High-Risk Loans (1): 85% - When the model predicted a loan as high-risk, it was correct 85% of the time
  * Recall:
    * Healthy Loans (0): 99% - The model identified 99% of all actual healthy loans
    * High-Risk Loans (1): 91% - The model identified 91% of all actual high-risk loans
  * Confusion Matrix:
    * True Negatives (correctly predicted healthy loans): 18,663
    * False Positives (healthy loans incorrectly predicted as high-risk): 102
    * False Negatives (high-risk loans incorrectly predicted as healthy): 56
    * True Positives (correctly predicted high-risk loans): 563

## Summary

The logistic regression model demonstrates strong performance in predicting credit risk, with an overall accuracy of 99%. 

For high-risk loans (class 1), which are more critical to identify correctly from a business perspective, the model achieves a recall of 91%. This is particularly important as it means the model can identify the majority of loans that will default, helping the company avoid potential losses. However, the precision for high-risk loans is slightly lower at 85%, indicating some healthy loans are being incorrectly flagged as high-risk.

For healthy loans (class 0), the model performs exceptionally well with 100% precision and 99% recall, meaning it rarely misclassifies borrowers who would repay their loans.

I recommend using this logistic regression model for the following reasons:
1. High overall accuracy (99%)
2. Strong recall for high-risk loans (91%), which is crucial for minimizing financial losses
3. Excellent performance in identifying healthy loans, ensuring creditworthy borrowers aren't wrongly denied

In a lending context, it's generally more important to correctly predict the high-risk loans (1's) than the healthy loans (0's), as the cost of approving a loan that defaults is typically higher than the opportunity cost of denying a loan to a creditworthy borrower. This model's strong recall for high-risk loans makes it particularly suitable for this business problem.

Potential improvements to consider would be addressing the class imbalance in the dataset, which might further improve the model's precision for high-risk loans.