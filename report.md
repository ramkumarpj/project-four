# Economic Recession - Report 

## Overview of the Analysis

* The goal is to create a Machine Learning model using historcial Treasury rates and Gross Domestic Product(GDP) data to predict US recession.

* Data Source - 

  1. 10 Years Treasury Historical Interest Rates since 1959 (Source : FRED API - Federal Reserve Bank of St.Louis)
  
  2. 2 Years Treasury Historical Interest Rates since 1974 (Source : FRED API - Federal Reserve Bank of St.Louis)
  
  3. 1 Year Treasury Historical Interest Rates since 1959 (Source : FRED API - Federal Reserve Bank of St.Louis)
  
  4. Gross Domestic Product (GDP) Data since 1959 (Source: BEA - US Bureau of Economic Analysis)

* Following data points are needed to build this model - 
 
  - 10 Years Minus 2 Years Historical Treasury Interest Rates
  - 10 Years Minus 1 Year Historical Treasury Interest Rates
  - Change in private inventories
   
* The target feature 'IS_RECESSION' is caculated using GDP quaterly growth rates. IS_RECESSION is represented as 'True' when GDP Growth rate is negative, otherwise it is recorded as 'False'.

* The data downloaded from files and API are loaded into Pandas DataFrames.

* The data was then split into training and test set.
  - The target column 'IS_RECESSION' was pulled into a seried named 'y'
  - All the other features were pulled into a dataframe named 'X'
  - Scikit-Learn 'train_test_split' function was used to split X and y to train and test data sets named X_train, y_train and X_test, y_test.

* Logistic Regression model from Scikit Learn was chosen to train and predict the recession
  - LogisticRegression model was created using solver named 'lbfgs' and random_state=42, test_size=.2 and stratify=y
 - LogisticRegression Model created was then fitted using training dataset - X_train and y_train.
  - The model is then used to predict recession of test dataset 'X_test'

## Results

* Logistic Regression Model :
    * Classification Report
      - Accuracy (0.98), 
      - IS_RECESSION False (No Recession) - Precision (0.98), and Recall (1.00).
      - IS_RECESSION True (Recession) - Precision (1.00), and Recall (0.50).

## Summary

* The optimized version of logistic regression model for predicting an economic recession based on difference in the interest rates of  long term and short term treasuries and change in private invetories is able to achieve an accuracy score of **98.07%**. The precision and recall for 'False' label is .98 and 1.00 respecitvely. The precision and recall for 'True' label is 1.0 and .50 respecitvely.


* The precision and recall score for Loan Status '0' are both 1, which means the model was able to correctly predict 'Healty Loan' labels. 

* The precision and recall score for Loan Status '1' are .87 & .89 respectievely so the model was not able to predict 'High-Risk Loan' as accurate as 'healthy loan' but it still has a good success rate.

**Recommends** Logistics Regression Model for predicting credit worthiness of borrowers

