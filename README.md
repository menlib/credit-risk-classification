OVERVIEW OF THE ANALYSIS

The purpose of the analysis is to use various techniques to train and evaluate a model based on loan risk. Dataset used is of historical lending activity from a peer-to-peer lending services company to build a model that can identify the creditworthiness of borrowers.

The main applicable information from the dataset is the loan status as it is used to classify credit risk predictions. Other financial information features such as loan size, interest rate, borrower income, debt to income ratio, number of accounts, derogatory marks and total debt are considered when predicting the loan status. 

There are two variables for the target values of loan status and with the use of value_counts function it is possible to predict whether the loan is healthy or it is at a high risk of defaulting. The first set of a variables holds a value of '0' and value_count of 75036 which indicates that the loan is healthy. The second set of a variables holds a value of '1' and value_count of 2500 which indicates that the loan is at a great risk of defaulting. 

The stages of the machine learning process were as follows:
Split the data into training and testing sets.
Create the labels set (y) from the loan status column.
Create the features (X) DataFrame from the remaining columns.
Create a Logistic Regression Model with the original data.
Evaluate the model's performance by generating a confusion matrix and printing the classification report. 

Logistic regression model is used as it models a binary outcome that can take two values, which in this case is healthy or high-risk loan. 

RESULTS

 Machine Learning Model 1: Logistic Regression
* Overall, the model does a great job at predicting both healthy and high-risk scores which can be drawn from the high accuracy score of 99% and balanced accuracy score of 95%. It performs extremely well for healthy loans with near perfect precision, recall and F1 score which may be due to the fact that the majority of the target values are for healthy loans. 
The overall accuracy of 99% suggests that the model makes correct predictions for most instances.
The macro average indicates good overall performance and also highlights the imbalance since healthy loans' metrics dominate due to its larger support.
This model has a recall score of 99% for the healthy loans and 91% for the high-risk loans. This means for all the instances where the loans were actually healthy, 99% of the times and  they were classified correctly and only 1% of the time they were classified as high-risk loan. On the other hand, for all the instances where the loans were in fact high-risk, they were classified correctly 91% of the times.
The F1 score for a healthy loan is 1 and for high-risk loan it is 0.88. The F1 score of 0.88 implies a good but not perfect balance between precision and recall.

SUMMARY

Based on the results and analysis, following are key takeaway points:
Although linear regression model returned high precision, recall and F1 scores for both healthy and high-risk loans, it may not be the most effective model especially in the context of imbalanced datasets where 97% of the target values are for the healthy loans. Hence, the model is the most effective at predicting healthy loans with a perfect F1 score and F1 score of 0.88 for high-risk loans suggesting a weaker performance. 


