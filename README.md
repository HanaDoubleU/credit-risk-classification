# credit-risk-classification
twentieth week's assignment

## overview of analysis
* The purpose of the following analysis is to (1) meaningfully interpret the steps in Credit_Risk/credit_risk_classification.ipynb and (2) truly understand its results and implications.
* The financial information in this data (Credit_Risk/Resources/lending_data.csv) is on 8 variables relating to the nature of the loans themselves and their surrounding circumstances:
  1. loan_size
  2. interest_rate
  3. borrowers_income
  4. debt_to_income
  5. num_of_accounts
  6. derogatory_marks
  7. total_debt
  8. loan_status (under which 0 represents healthy and 1 represents high-risk)
  What I needed to predict was the 8th variable, loan_status. In other words, I needed to see how the other variables could determine a healthy or high-risk loan.
* Further information on each variable/column in lending_data.csv:
  * All of the values in lending_data.csv are floats.
  * The data is not scaled, as nearly half of the variables' means are far from 0, a couple of their standard deviations are far from 1, and the ranges (demonstrated by the variables' drastically differing minimums and maximums) vary greatly.
  * There is 1 column which is a boolean: It is loan_status, the assigned target/y under which 0 specifies a healthy loan and 1 specifies a high-risk loan.
  * There is 1 column which has 1 of 4 values: It is derogatory_marks under which the values range from 0 to 3.
  * There is 1 column which has 1 of 17 values: It is num_of_accounts under which the values range from 0 to 16.
  * The remaining 5 columns which have not yet been mentioned can be any number; though some like loan_size, interest_rate, and debt_to_income can be decimals.
* Stages of machine learning process in Credit_Risk/credit_risk_classification.ipynb:
  1. I assigned the column which I wanted to predict as y, or my target.
  2. I assigned the remaining columns as X, or my features.
  3. I split the data for training data and testing data.
  4. I created a logistic regression model with the training data.
  5. I generated predictions for the testing data (i.e. X_test) with the logistic regression model fitted to the training data.
  6. I made a confusion matrix. Then I made a classification report including the confusion matrix. These allowed for me to truly understand the results of the linear regression model.
* Methods which I used include 'LogisticRegression'.

## results
* this logistic regression model:
  * accuracy score: The accuracy score in the classification report indicates the proportion of <em>all</em> correct predictions for either result over <em>all</em> predictions. For example, the accuracy score for this model in general is ~0.99, signifying that ~99% of this model's predictions are correct. To understand the ~1% of predictions where this model seems to fall short, the following parameters below can be consulted:
    * precision: Precision in the classification report indicates the proportions of correct predictions over all of that specific result's predictions, whether they are actual positives or not. For example, the precision for healthy loans is 1.00, signifying that this model was able to predict all of the actual 0s, while the precision for high-risk loans is 0.87, signifying that this model was able to predict or detect only 87% of the actual 1s.
    * recall scores: Recall scores indicate the proportions of correct predictions over all of that specific result's actual positives. For example, the recall score for healthy loans is 1.00, signifying that this model predicted all of the actual 0s in the data, while the recall score for high-risk loans is 0.95, signifying that this model predicted only 95% of the actual 1s in the data. The remaining 5% signifies the false negatives (i.e. high-risk loans mistakenly predicted to be healthy loans).

## summary
* This logistic regression model seems to perform best when predicting healthy loans because its precision and recall in 0s is exactly 1.00, meaning it yeilds no false positives or negatives. As such, I know that it would perform best on this front.
* It should be noted, though, that this logistic regression model's performance depends on the problem which its user is trying to solve. For example, while it predicts healthy loans perfectly, it predicts high-risk loans not-so-perfectly. Not-so-perfectly yet -- still -- very well, because of the relatively high values it yeilds for precision and recall in 1s. Nonetheless, I would not recommend this logistic regression model for users who wish to predict high-risk loans.
