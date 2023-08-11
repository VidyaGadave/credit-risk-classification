# Credit Risk Classification

This analysis looked to create a model to identify the creditworthiness of borrowers as being either a healthy or high risk loan.

Given the binary outcome the model was seeking to predict (healthy or high risk), logistic regression was used for the analysis.

## Data overview:

A data set of historical lending activity from a peer-to-peer lending services company was used to build the model.
The dependent variable (y value) was loan status, indicating whether a loan was healthy or high risk.
The independent variables (x values) were loan size, interest rate, borrower income, debt to income, number of accounts, derogatory marks, and total debt.


Analysis overview:
1. The dependent variable (loan status) was removed from the independent variables.
2. The data was then split into training and testing datasets.
3. After which a logistic regression model was created and fitted with the training data.
4. The trained model was then used to make predictions of loan status using the test data.
5. The performance of the model was evaluated.
6. Two different logistic regression models were created:

The first using the original data set.
The second using resampled training data that over-sampled high risk loans (the minority group in this data set).

## Results
### Machine Learning Model 1: Logistic Regression Model with the original data

precision for healthy loan : 1.00       
recall for healthy loan : 0.99  
f1-score for healthy loan : 1.00   
precision for High Risk Loans :  0.85         
recall for High Risk Loans : 0.91   
f1-score for High Risk Loans :  0.88   


### Machine Learning Model 2: Logistic Regression model with resampled training data

precision for healthy loan : 1.00       
recall for healthy loan : 0.99  
f1-score for healthy loan : 1.00   
precision for High Risk Loans :  0.84         
recall for High Risk Loans : 0.99  
f1-score for High Risk Loans :  0.91   


## Summary
While both models accurately predict healthy loans, they differ in their ability to predict high risk loans.
Both models score the same on precision in predicting healthy loan as 100% however the precision for high risk loans are at 0.85 and 0.84.

Based on the analysis undertaken, model 2 (which used resampled training data) is the strongest performing model in predicting whether a loan is healthy or high risk. Given its performance I would recommend the company use model 2. I would ensure they were aware the model may incorrectly classify some healthy loans as high risk, so this should be taken care of. 
