## Overview of the Analysis

With the use of machine learning, we will analyze the financial dataset of historical lending activity to determine the risk of loans.

The dataset holds over 77K datapoints which include factors important to credit loans - such as loan size, interest rate, borrower income, debt to income, number of accounts, derogatory marks, total debt, and loan status. The loan status will provide color as to if a loan is heathy or high risk of defaulting. In the loan status column, 0 represents healthy loans, while 1 represents a loan being high risk.

The data was split into training and testing sets, and the information in the training set was put through a logistic regression model, and that same model was applied to the testing set. The purpose was to determine if a loan would be high or low risk. The results are labeled below in the "Machine Learning Model 1" details.

The data was then resampled for the training dataset with the use of RandomOverSampler. With the new training dataset, a new logistic regression model was created. The results are listed under "Machine Learning Model 2".


* Purpose of the analysis
* Basic information about the variables you were trying to predict (e.g., `value_counts`).
* Describe the stages of the machine learning process you went through as part of this analysis.
* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).
 
## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Healthy (Loan Status: 0): 
    - Precision: 1.00
    - Recall: 1.00
    - F1-score: 1.00
    - Support: 18,759
  * High-Risk Loans (Loan Status: 1):
    - Precision: 0.87
    - Recall: 0.89
    - F1-score: 0.88
    - Support: 625
  * Accuracy: 0.99
  * Macro Average:
    - Precision: 0.94
    - Recall: 0.94
    - F1-Score: 0.94
    - Support: 19,384
  * Weighted Average:
    - Precision: 0.99
    - Recall: 0.99
    - F1-Score: 0.99
    - Support: 19,384

* Machine Learning Model 2:
  * Healthy (Loan Status: 0): 
    - Precision: 1.00
    - Recall: 1.00
    - F1-score: 1.00
    - Support: 18,759
  * High-Risk Loans (Loan Status: 1):
    - Precision: 0.87
    - Recall: 1.00
    - F1-score: 0.93
    - Support: 625
  * Accuracy: 1.00
  * Macro Average:
    - Precision: 0.94
    - Recall: 1.00
    - F1-Score: 0.96
    - Support: 19,384
  * Weighted Average:
    - Precision: 1.00
    - Recall: 1.00
    - F1-Score: 1.00
    - Support: 19,384

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* The Machine Learning Model 2 had better results for high-risk loans than the first model. The healthy loans had the same output. As such, based on the classification report, the 2nd model predicted slightly better for high-risk loans recall with no false negatives. 
* When it comes to which is better - determining the right amount of 0s or 1s, it would determine on what the person is trying to calculate. Both models have pretty high precision and recall to determine this, but a banker may care more about the healthy loans, while a credit collector may be more focused on the high risk of defaulting.
