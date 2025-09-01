## Loan Default Prediction:

## Problem Statement:
  Loan defaults pose significant challenges to financial institutions by directly impacting their profitability and financial stability.
  High default rates can lead to substantial losses, reduce available capital for future lending, and increase the cost of borrowing, ultimately affecting the institution's ability to serve its customers and maintain investor confidence.
This study aims to demonstrate how data can be leveraged to mitigate the risk of loan defaults. By utilizing data analysis and machine learning, the lending decision-making process can be improved, thereby reducing the incidence of loan defaults.


## Business KPI:
### Our Goal:
  We analyze the performance of these models according to our business KPIs. There can be various KPIs for risk analysis; in this study, we focus more on:

  - Default rate: We need to decrease the rate of default by being able to predict these applications.

  - Approval rate: We need to increase the approval rate for clients who will repay.

In this scenario, I choose decreasing the default rate to be more critical.

## Exploratory Data Analysis (EDA):
  Our data exists in two parts:
  
  1. Current applications: data covers more than 300,000 applications and contains different information about the applicant, the application process, and whether the client was able to repay or default.

  2. Previous applications: the data covers 1670214 applications and contains similar information, however, there is no information about the client's repayment.
    EDA process enabled us to filter unnecessary data for our analysis.
    We found some features like EXT_DOC_i have significant influence on the dependent variable. 


## Feature Engineering:
  For feature engineering and feature extraction, we make use of insights gained from EDA, and along the way, we apply two methods to help with data modelling:
  
  Principal Component Analysis (PCA).
  
  Feature extraction using a random forest.
  
  Some transformations were done on some features to get more stable ones (e.g., DAYS_BIRTH).


## Modeling:
### Our Approach: 
  For this problem, We will utilize tree-based models for their interpretability, flexibility, and robustness, making them well-suited for our problem. 
  Using our data, we first trained a decision tree. Then, we advanced to ensemble techniques to get better outcomes.
  Bagging Method:  Random Forest.
  Boosting Method: XGBoost.

  We also trained a logistic regression model to act as a base model.

  ## Model Evaluation:
  ### Models Performance:
  We will evaluate the model using precision, recall, and F1 score.
  The highest f1 score didn't exceed 27% was obtained by random forest model trained on features extracted by another random forest model.
  Random forest model trained on PCA components achieved the highest recall 62%, which is more suitable for default rate KPI.
  XGboost achieved the highest precision across all versions (15% and 17%), which can be good for the acceptance rate KPI.
  Despite the low metrics, these models show an advance in performance against our base model (logistic regression in our case).


##Future Improvements:

Data was highly imbalanced, though tree models can deal with this issue, applying sampling techniques can improve the model.
We can work on a semi-supervised way using deep learning model, which can improve the predictive power, but  then we sacrifiy the interpretability benefit.
More data engineering can be done by combining the two datasets.





  



