# credit-risk-classification


### OVERVIEW

The purpose of this analysis is to to analyze the creditworthiness of borrowers. The model uses the data of 77,535 borrowers, each with the following financial information:
    Loan size
    Interest rate
    Borrower income
    Debt to income (decimal ratio)
    Number of accounts
    Derogatory marks
    Total debt
    Loan status

The end goal is to develop a predictive model based on loan risk.

I began by generating a dataframe from the csv of borrower data -- then, split it into two variables, x and y. Since we're working off of whether or not someone is a risk, we have y set as "loan_status" and x as everything else.
Next, we split the data into distinct training and testing datasets. We use the training dataset to analyze the performance of our model, and the testing dataset to generate our results after testing.

Next, we plug our training data into a logistic regression model. This is how we model the probability of an outcome (such as whether a borrower is a risk) based on our inputs. We fit the model to the training data, make predictions, and save them into another dataframe.

Now, we can view the results of our testing. We generate a confusion matrix based on the y_test data and our predictions dataframe -- as well as printing out a classification report. The confusion matrix allows us to see the performance of our algorithm, and the classification report gives an overall view of the metrics of our algorithm, such as it's accuracy in different classification metrics.



### RESULTS

Creditworthy Borrower
 * Precision: 1.0
 * Recall: 1.0
 * F1-Score: 1.0
 * Support: 18759

High Risk Borrower
 * Precision: 0.87
 * Recall: 0.89
 * F1-Score: 0.88
 * Support: 625

Model Accuracy
 * F1-Score: 0.99
 * Support: 19384

 Model Macro Avg: 
 * Precision: 0.94
 * Recall: 0.94
 * F1-Score: 0.94
 * Support: 19384

 Model Weighted Avg:
 * Precision: 0.99
 * Recall: 0.99
 * F1-Score: 0.99
 * Support: 19384


The f1-score is a measure of how well our model is able to predict outcomes. From our results we can see that model is able to predict healthy loan borrowers exceedingly well, with an f1-score of 1.0. This is extremely good! However, it's a bit worse at predicting the high-risk borrowers with an f1-score of .88.



### SUMMARY

Overall, our accuracy score has an f1-score has of .99, meaning that this model can predict the creditworthiness of a borrower 99% of the time. However, this is heavily skewed in favor of creditworthy borrowers. I would recommend only using the model for assessing whether or not someone is a creditworthy borrower, as the model for predicting high risk borrowers needs to be further trained and tuned -- <90% accuracy is simply not good enough as it seems more important to assess whether someone is high risk or not. 

