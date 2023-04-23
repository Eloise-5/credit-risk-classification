# Credit Risk Classification - Analysis Report

## Overview

The purpose of this analysis is to understand whether a borrower is considered to have healthy (0) or high risk (1) loans. This may support the classification of any potential future customers when predicting their creditworthiness. 

The original data provided included historical lending activity from 77k+ borrowers, including their loan size, interest rate, income, debt to income, number of accounts, any derogatory marks, as well as their total debt. From this information, we need to understand if a future borrower with similar characteristics is considered to be a healthy or high risk borrower, ultimately assessing their risk of default.   

To perform this analysis, the data was split into training and testing groups. This was then utilised in a Logistic Regression Model (SKLearn) to predict (0) or (1) outcomes. 

The same was then performed after resampling the training data. The Random Over Sampler module from imbalanced-learn was utilised so that an equal number of healthy and high risk loans were included in this regression. 


## Results

### Logistic Regression Model - Original Data
* Precision
  * Healthy Loan - 100%
  * High Risk Loan - 87%
* Recall 
  * Healthy Loan - 100%
  * High Risk Loan - 89%
* F1 Score
  * Healthy Loan - 100%
  * High Risk Loan - 88%
* Overall Accuracy - 99%

### Logistic Regression Model - Resampled Data
* Precision
  * Healthy Loan - 90%
  * High Risk Loan - 99%
* Recall 
  * Healthy Loan - 99%
  * High Risk Loan - 89%
* F1 Score
  * Healthy Loan - 95%
  * High Risk Loan - 94%
* Overall Accuracy - 94%



## Summary

The ultimate aim of the analysis was to accurately predict future borrower's likeliness to default on their loans (in layman's terms, whether they would be a 1 or not). This places greater importance on predicting a '1' within the data. Whilst the original logistic regression provided a higher overall accuracy score (0.99 compared with 0.94), the 'high risk loan' precision and f1 scores were greatly improved with the use of the oversampling module. Because of this, the second model should be used for any further analysis. 
