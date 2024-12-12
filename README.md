# credit-risk-classification
twentieth week's assignment

## overview of analysis
* The purpose of the following analysis is to...
* The financial information in this data (Credit_Risk/Resources/lending_data.csv) is on...and what I needed to predict was...
* Further information like value_count of each variable:
* Stages of machine learning process in Credit_Risk/credit_risk_classification.ipynb.
* Methods which I used include 'LogisticRegression' and other algorithms, such as...

## results
* this logistic regression model:
  * accuracy score:
  * precision:
  * recall scores:

## summary
* This logistic regression model seems to perform best when predicting healthy loans because its precision and recall in 0s is exactly 1.00, meaning it yeilds no false positives or negatives. As such, I know that it would perform best on this front.
* It should be noted, though, that this logistic regression model's performance depends on the problem which its user is trying to solve. For example, while it predicts healthy loans perfectly, it predicts high-risk loans not-so-perfectly. Not-so-perfectly yet -- still -- very well, because of the relatively high values it yeilds for precision and recall in 1s. Nonetheless, I would not recommend this logistic regression model for users who wish to predict high-risk loans.
