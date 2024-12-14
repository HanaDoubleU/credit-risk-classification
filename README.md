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
  * accuracy score: The accuracy score in the classification report indicates the proportion of <em>all</em> correct predictions for either result over <em>all</em> predictions. For example, the accuracy score for this model in general is ~0.99, signifying that ~99% of this model's predictions are correct. To understand the ~1% of predictions where this model seems to fall short, the following parameters below can be consulted:
    * precision: Precision in the classification report indicates the proportions of correct predictions over all of that specific result's predictions, whether they are actual positives or not. For example, the precision for healthy loans is 1.00, signifying that this model was able to predict all of the actual 0s, while the precision for high-risk loans is 0.87, signifying that this model was able to predict or detect only 87% of the actual 1s.
    * recall scores: Recall scores indicate the proportions of correct predictions over all of that specific result's actual positives. For example, the recall score for healthy loans is 1.00, signifying that this model predicted all of the actual 0s in the data, while the recall score for high-risk loans is 0.95, signifying that this model predicted only 95% of the actual 1s in the data. The remaining 5% signifies the false negatives (i.e. high-risk loans mistakenly predicted to be healthy loans).

## summary
* This logistic regression model seems to perform best when predicting healthy loans because its precision and recall in 0s is exactly 1.00, meaning it yeilds no false positives or negatives. As such, I know that it would perform best on this front.
* It should be noted, though, that this logistic regression model's performance depends on the problem which its user is trying to solve. For example, while it predicts healthy loans perfectly, it predicts high-risk loans not-so-perfectly. Not-so-perfectly yet -- still -- very well, because of the relatively high values it yeilds for precision and recall in 1s. Nonetheless, I would not recommend this logistic regression model for users who wish to predict high-risk loans.
