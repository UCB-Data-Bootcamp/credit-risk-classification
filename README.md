# credit-risk-classification
Module 20 Challenge

# Credit Risk Analysis Report

## Analysis overview
* We first load the data. The data provides loan and borrower information and whether a loan was approved. Dataset collumns include:
    * loan_size (float)
    * interest_rate (float)
    * borrower_income (int)
    * debt_to_income  (float)
    * num_of_accounts (int)
    * derogatory_marks (int)
    * total_debt (int)
    * loan_status (int, binary, target)

* Setting loan_status as target and the rest as input features for our model
* Create test and train datasets
* Create model using the train set
* Validate the model with the test set
* Evaluate accuracy of model with score, confusion matrix and classification reports
* Create a new oversampled dataset for loan approvals and rerun the Regression algorithm

## Results
* For our model we use all the relevant features regarding the loan and the borrower (listed above).
* The high risk loans are way higher than the healthy ones, so our model might have some precision issues.
* After running the fit we see that, based on the confusion marix, our model predicts pretty well the healthy loans but we get FP to be twice as many as the FN which are less consequential when it comes to a loan.
* In order to increase or FP/FN ratio we oversample our dataset in order to increase our sample size and allow some overfitting in order to improve our precision.
* We then run the regression over the whole dataset and the performance improves to a similar FP/FN ratio

## Summary
Oversampling is a great tool in case we have a very limited dataset for a particular target feature. In this case even though we had a failrly large number of high risk loand ~2500, the algorithm was still providing us with a large number or false positives. That can be risky for an organizsation that provides loans. By increasing the number of high risk samples we were able to improve our model and provide a more accurate prediction of high risk loans

