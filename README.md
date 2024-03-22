<h1>CUSTOMER CHURN PREDICTON</h1>

Customer churn refers to when customers stop using a company's products or services. It's like when you stop going to your favorite ice cream shop or switch to a different phone company. Churn is important because losing customers can hurt a company's business. It's like losing money because fewer people are buying their stuff. Companies want to keep customers happy and keep them coming back because it's easier and cheaper than finding new ones. So, they use things like discounts or better service to try to stop customers from leaving. Churn is like a big puzzle for companies to solve so they can keep their customers happy and their business growing.



![download](https://github.com/ArnavGhosh999/CODSOFT/assets/133378610/b96b701c-b31c-40b4-a3d6-3105baaff760)

## Objectives:
<h5>- Finding the % of Churn Customers and customers that keep in with the active services.</h5>
<h5>- Analysing the data in terms of various features responsible for customer Churn
</h5>
<h5>- Finding a most suited machine learning model for correct classification of Churn and non churn customers.</h5>

<h3>Correlation Heatmap</h3>

![download](https://github.com/ArnavGhosh999/CODSOFT/assets/133378610/a99801d0-f59d-47cf-82e9-5a35e70e120b)

<h3>Barplot for how many have churned v/s not churned</h3>
<h3>~Roughly around 79-80% have not churned only around 20-21% have churned</h3>
<h4>Index - 0 </h4>
<h4>Exited - 1</h4>

![download](https://github.com/ArnavGhosh999/CODSOFT/assets/133378610/7da95035-00b0-465e-9150-bee067fd1ff6)

<h3>"Female customers have churned more than male customers</h3>

![download](https://github.com/ArnavGhosh999/CODSOFT/assets/133378610/b6cc76cd-e2e5-49ca-8408-bbd3b989e489)


![download](https://github.com/ArnavGhosh999/CODSOFT/assets/133378610/6499f970-37fa-4a4d-9d05-3550b22bf59d)


![download](https://github.com/ArnavGhosh999/CODSOFT/assets/133378610/a8a5a96e-dfb0-4728-a661-43e4e1749694)
## Customers having brought more number of products have more chances of getting churned.


<h1>Now we look into the accuracy for predicting the churn rate</h1>
<h5>-Precision: Measures the accuracy of positive predictions made by the model.
</h5>
<h5>-Recall: Measures the proportion of actual positives that were correctly identified by the model.
</h5>
<h5>-F1-score: Represents the balance between precision and recall, providing an overall measure of a model's performance.
</h5>


## Logistic Regression
```
lr_precision = precision_score(y_test, lr_pred)
lr_recall = recall_score(y_test, lr_pred)
lr_f1 = f1_score(y_test, lr_pred)
print("Logistic Regression Precision:", lr_precision*100.0,"%")
print("Logistic Regression Recall:", lr_recall*100.0,"%")
print("Logistic Regression F1-score:", lr_f1*100.0,"%")

Accuracy for predicting churn
-Logistic Regression Precision: 55.24%
-Logistic Regression Recall: 20.10%
-Logistic Regression F1-score: 29.48%
```
## Random Forest:
```
rf_precision = precision_score(y_test, rf_pred)
rf_recall = recall_score(y_test, rf_pred)
rf_f1 = f1_score(y_test, rf_pred)
print("\nRandom Forest Precision:", rf_precision*100.0,"%")
print("Random Forest Recall:", rf_recall*100.0,"%")
print("Random Forest F1-score:", rf_f1*100.0,"%")

Accuracy for predicting churn
-Random Forest Precision: 75.82%
-Random Forest Recall: 47.07%
-Random Forest F1-score: 58.08%
```

## Gradient Boosting:
```
gb_precision = precision_score(y_test, gb_pred)
gb_recall = recall_score(y_test, gb_pred)
gb_f1 = f1_score(y_test, gb_pred)
print("\nGradient Boosting Precision:", gb_precision*100.0,"%")
print("Gradient Boosting Recall:", gb_recall*100.0,"%")
print("Gradient Boosting F1-score:", gb_f1*100.0,"%")

Accuracy for predicting churn
-Gradient Boosting Precision: 75.00%
-Gradient Boosting Recall: 48.85%
-Gradient Boosting F1-score: 59.17%
```
## What do we mean by the percentage values given above ?

```
Logistic Regression:
-Precision: 0.55
This means that when the logistic regression model predicts a customer will churn, it is correct about 55% of the time.
-Recall: 0.20
This means that the logistic regression model correctly identifies about 20% of all actual churn cases.
-F1-score: 0.29
The F1-score is the harmonic mean of precision and recall. It provides a balanced measure of model performance. In this case, the logistic regression model's F1-score is 0.29, indicating a moderate level of overall performance.

Random Forest:
-Precision: 0.76
The random forest model has a higher precision compared to logistic regression, meaning it correctly predicts churned customers more often.
-Recall: 0.47
The random forest model correctly identifies about 47% of all actual churn cases, which is higher than logistic regression.
-F1-score: 0.58
The F1-score for the random forest model is 0.58, indicating a better balance between precision and recall compared to logistic regression.

Gradient Boosting:
-Precision: 0.75
Similar to random forest, the gradient boosting model has high precision, correctly predicting churned customers about 75% of the time.
-Recall: 0.49
The gradient boosting model's recall is also higher than logistic regression, correctly identifying about 49% of all actual churn cases.
-F1-score: 0.59
The F1-score for the gradient boosting model is 0.59, indicating a good balance between precision and recall, and a higher overall performance compared to logistic regression.
```

## ROC Curve

<h3>What is an ROC Curve?</h3>
<h4>-
The ROC curve shows how good our model is at distinguishing between two things, like customers who leave and those who stay. It's like a report card that tells us if our model is doing a good job or not.

</h4>

![download](https://github.com/ArnavGhosh999/CODSOFT/assets/133378610/16346f03-c3ae-49df-8f5e-0898c6b7914d)


