# Module 20 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.
The purpose of this analysis was to develop and evaluate machine learning models to predict the risk level of loans—specifically whether a loan is likely to be a healthy loan (or low-risk) vs. a high-risk loan. This prediction is crucial for financial institutions to minimize potential losses and manage risk effectively.

* Explain what financial information the data was on, and what you needed to predict.
The dataset used for this analysis contained financial information on various loans. This included factors such as loan size, interest rates, borrower income, debt-to-income ratio, number of accounts, total debt, derogatory marks and loan status. The objective was to predict the target variable, which indicates whether a loan is healthy (0) or high-risk (1).

* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
Target Variable:
0 (Healthy Loan): Represents loans that are likely to be repaid without issues.
1 (High-Risk Loan): Represents loans that have a higher likelihood of default.

Distribution of Target Variable:
The dataset had a significant class imbalance, with a much higher proportion of healthy loans (0) compared to high-risk loans (1).

* Describe the stages of the machine learning process you went through as part of this analysis.
1. Data Preprocessing: Cleaned and prepared the data for modeling by handling missing values, encoding categorical variables, and normalizing numerical features.Performed exploratory data analysis to understand the distribution of features and the target variable.

Model Selection: Leveraged LogisticRegression as the model to train. 

Model Training: Split the data into training and testing sets.Trained each model on the training data and used cross-validation to assess performance stability.

Model Evaluation:Evaluated the models on the test data using metrics such as accuracy, precision, recall, and F1-score to understand how well each model predicted the healthy and high-risk loans.

* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any other algorithms).
The Logistic Regression model shows overall high performance, particularly in predicting healthy loans, which comprise the majority of the dataset. This model strikes a good balance between predicting both classes effectively. However, if the focus shifts more towards high-risk loans, additional models or adjustments may be considered to enhance recall and precision for that class.

## Results

Using bulleted lists, describe the accuracy scores and the precision and recall scores of all machine learning models.

Machine Learning Model 1: Logistic Regression

Accuracy: 99%
Precision (Healthy Loan): 1.00
Recall (Healthy Loan): 0.99
F1-Score (Healthy Loan): 1.00
Precision (High-Risk Loan): 0.85
Recall (High-Risk Loan): 0.91
F1-Score (High-Risk Loan): 0.88

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:

* Which one seems to perform best? How do you know it performs best?
While we did not leverage other machine learning models, based on the evaluation metrics, Logistic Regression appears to perform incredibly accurately. This model achieved a high accuracy of 99%, with excellent precision and recall scores for predicting healthy loans (0). The model also performed well in predicting high-risk loans (1), with a precision of 85% and a recall of 91%.

* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )
The performance of the model depends on the specific problem we are trying to solve. If the primary goal is to accurately predict healthy loans (to minimize false positives), the Logistic Regression model is highly effective. However, if the focus is on correctly identifying high-risk loans (to minimize potential defaults), the slight trade-off in precision for high-risk loans may need to be considered.

If you do not recommend any of the models, please justify your reasoning.
