# Module 20 Report

## Overview of the Analysis

* **Purpose of the analysis** - The goal of this analysis is to determine if the logistic regression machine learning model can more accurately predict healthy loans than high-risk loans using the original dataset or a dataset that is resampled to increase the size of the minority class.

* **Data Source** - the dataset used to perform the analsys consists of information on 77,536 loans. The data has columns for loan_size, interest_rate, borrower_income, debt_to_income ratio, number_of_accounts, derotatory_marks, total_debt, and loan_status. The column we attempted to predict with our analysis is the `loan_status`. The data in the remaining columns was used as features to train the data and inform the predictions.

* **Stages of the machine learning process** The stages of the machine learning process are very scripted. If followed in order, they provide us with an accurate assessment of the model's ability to make predictions. The stages of the machine learning process are as follows:

    - Prepare the data - Import the file, establish the DataFrame, evaluate the columns and features. 
    
    - Separate the data into features and labels - The labels are what we are attempting to predict. Is the status of the loan healthy (0) or high-risk (1)? The features are all of the remaining data we will use to train and test the model.
    
    - Use the train_test_split function to separate the features and labels data into training and testing datasets. 
    
    - Import the machine learning model from the library - In this instance, we will be importing LogisticRegression from SKLearn. 
    
    - Instantiate the model.
    
    - Fit the model using the training data.
    
    - Use the model to make predictions using the features test data.
    
    - Evaluate the predictions - Evaluations are done by calculating and comparing metrics like accuracy score, a confusion matrix, and a classification report.
    
* **Machine Learning Methods Utilized** - 

    The primary model used in this analysis is:

    - LogisticRegression model from SKLearn
    
    Supporting functions used in this analysis are:
    
    - train_test_split from SKLearn
    
    Models are evaluated using the following functions:

    - confustion_matrix from SKLearn
    - classification_report from SKLearn

## Results

Using bulleted lists, describe the accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
    - Accuracy score: 0.99
    - Precision scores: Label 0: 1.00 Label 1: 0.84
    - Recall scores: Label 0: 0.99 Label 1: 0.94

## Summary

The logistic Regression model performed well. For the 0 class, both the precision and recall were extremely close to perfect. For the 1 class (high-risk loans), the model's precision is 0.84 and the recall is 0.94. This indicates that the model more often gives false positives than false negatives.

Given this information, it appears the Logistic Regression model does a great job at predicting both healthy and high-risk loans, given the features that are used to train the data. Although the model seems promising, it would need to be evaluated against different sets of data to confirm that it should be put into use for predicting the health status of loans