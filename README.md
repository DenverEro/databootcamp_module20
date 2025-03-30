# Credit Risk Analysis

## Overview
This project applies machine learning to assess credit risk using historical lending data from a peer-to-peer lending services company. The goal was to build a model that accurately predicts whether a loan is healthy or high-risk.

## Method
- Used logistic regression to create a binary classification model
- Features included loan size, interest rate, borrower income, debt-to-income ratio, number of accounts, derogatory marks, and total debt
- Target variable was loan status (0 = healthy loan, 1 = high-risk loan)
- Split data into training and testing sets
- Evaluated model performance using confusion matrix and classification metrics

## Results
- **Accuracy:** 99%
- **Precision:** 
 - Healthy loans: 100%
 - High-risk loans: 85%
- **Recall:**
 - Healthy loans: 99%
 - High-risk loans: 91%

The model demonstrates strong performance in identifying both healthy and high-risk loans, with particularly good recall for high-risk loans, which is crucial for minimizing financial losses in lending decisions.

## Detailed Report
For a comprehensive analysis of the model performance and detailed findings, please refer to the [Credit Risk Analysis Report](./report-template.md) in this repository.