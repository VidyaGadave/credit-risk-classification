# Credit Risk Classification

This analysis looked to create a model to identify the creditworthiness of borrowers as being either a healthy or high risk loan.

Given the binary outcome the model was seeking to predict (healthy or high risk), logistic regression was used for the analysis.

## Data overview:

A data set of historical lending activity from a peer-to-peer lending services company was used to build the model.
The dependent variable (y value) was loan status, indicating whether a loan was healthy or high risk.
The independent variables (x values) were loan size, interest rate, borrower income, debt to income, number of accounts, derogatory marks, and total debt.
Analysis overview:

The dependent variable (loan status) was removed from the independent variables.
The data was then split into training and testing datasets.
After which a logistic regression model was created and fitted with the training data.
The trained model was then used to make predictions of loan status using the test data.
The performance of the model was evaluated.
Two different logistic regression models were created:

The first using the original data set.
The second using resampled training data that over-sampled high risk loans (the minority group in this data set).

## Results
### Machine Learning Model 1: Logistic Regression Model with the original data

The model has a balanced accuracy score of 0.99, indicating it is performing well predicting whether a loan is healthy or high risk.
The model accurately predicts healthy loans, with a precision 1.00 , recall 0.99 and f1-score of 1.00. However the model is less accurate at predicting high risk loans, with lower precision (at 0.85), recall (at 0.91), and f1-score (at 0.88).
Precision looks at when the model predicts a high risk loan, how often it correctly does so. When this model predicts a high risk loan, it is correct 87% of the time. Indicating there are some healthy loans being incorrectly classified as high risk.


### Machine Learning Model 2: Logistic Regression model with resampled training data

This is a stronger performing model, with the balanced accuracy score sitting at its maximum value of 1.00 (rounded to two decimal places).
As with the previous model it can accurately predict healthy loans, with precision, recall, and an f1-score of 1.00.
However the model is less accurate at predicting high risk loans, with lower precision (at 0.86), recall (at 0.90), and f1-score (at 0.88).
Precision for high risk loans remains the same as the previous model (at 0.86). Which means that some healthy loans are being classified as high risk.


## Summary
While both models accurately predict healthy loans, they differ in their ability to predict high risk loans.

Both models score the same on precision in predicting high risk loans (at 0.85 and 0.86), meaning some healthy loans are being predicted as high risk. Which could potentially run the risk of losing business as a result.

Based on the analysis undertaken, model 2 (which used resampled training data) is the strongest performing model in predicting whether a loan is healthy or high risk. Given its performance I would recommend the company use model 2. But in recommending this I would ensure they were aware the model may incorrectly classify some healthy loans as high risk, so this could be an area they monitor. Future re-training of the model may also help to increase the precision in predicting high risk loans.

