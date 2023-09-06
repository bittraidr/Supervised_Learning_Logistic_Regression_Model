# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.

The purpose of this analysis is to identify the creditworthiness of potential loan borrowers. 

* Explain what financial information the data was on, and what you needed to predict.

The financial information was on loan size, interest rate, borrower income, debt to income, number of accounts, derogatory marks, and total debt. The goal was to predict the loan status, which became the target values. 0 represents a healthy loan and 1 represents a high risk loan that could default. 

* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).

There were 75036 healthy loans and 2500 high risk loans in the data set. 
0    75036
1     2500

* Describe the stages of the machine learning process you went through as part of this analysis.

After reading in the data from the csv file, I separated the data into y, labels and x, features. Then checked the balance of y to get an idea of how imbalanced the data actually is. I then defined X_train, X_test, y_train, y_test train-test-split, passing in X features and y labels with a random state of 1 to split the data. Following this, I instantiated the Logistic Regression model and fit the model using training data passing in X_train and y_train. Following fitting the model, I defined another variable, prediction, and set it equal to my fit classification model with .predict and passed in the X_test variable. From here I checked the balanced accuracy score passing in the y_test and prediction. With the same data I generated a confusion matrix then printed my results with a classification report. 

* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).

I used LogisticRegression initially with the imbalanced data. Then used RandomOverSampler to over sample and balance the previously imbalanced data. This allowed me to have the same amount of healthy loans as high risk loans.  
## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Description of Model 1 Accuracy, Precision, and Recall scores.
  
    * Accuracy: 0.9520479254722232
    * Precision: 0.85
    * Recall: 0.91


* Machine Learning Model 2:
  * Description of Model 2 Accuracy, Precision, and Recall scores.
  
    * Accuracy: 0.9936781215845847
    * Precision: 0.84
    * Recall: 0.99
## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

    -  The Machine Learning Model 2 preformed best here, as the data was initially very imbalanced. Oversampling the high risk loans allowed the model to more accurately, Model 2 was 99% compared with 95% with Machine Learning Model 1. In this instance it is more important to predict the high risk loans accurately because this is where loss is most likely to occur. The vast majority of our data was healthy loans and a small portion was high risk, I needed a larger sample in order to adequately make a prediction.    

If you do not recommend any of the models, please justify your reasoning.
