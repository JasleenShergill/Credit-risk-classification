## Overview of the Analysis

The goal of this analysis was to develop a supervised machine learning model to predict whether a loan is healthy or high-risk. Accurate predictions of loan status are crucial for financial institutions to minimize the risk of default and optimize their lending strategies.

## Financial Information and Prediction Target
The dataset consisted of 77,500 rows with the following financial information:

-Loan size    
-Interest rate    
-Borrower's income    
-Debt-to-income ratio    
-Number of accounts    
-Derogatory marks    
-Total debt    
-Loan status (healthy or high-risk)    
-Out of the total loans, 75,000 were labeled as healthy, and 2,500 were labeled as high-risk.    

Machine Learning Process
To build the model, the following steps were taken:

## Data Preparation:

The data was split into labels (loan_status) and features (the remaining columns).

## Data Splitting: 
The data was divided into training and testing sets using the train_test_split function from sklearn.
## Model Selection: 
A Logistic Regression model from sklearn was chosen, using the Limited-memory BFGS ('lbfgs') solver. Logistic Regression was selected for its efficiency in binary classification tasks.
## Model Training: 
The model was trained using the training data (X_train and y_train).
## Prediction: 
The model made predictions on the test data (X_test).
## Evaluation: 
The model's predictions were compared with the actual test labels to evaluate its        performance.This was done using metrics such as accuracy, precision, and recall.

## Results

-Accuracy: 0.99185    
-Balanced Accuracy: 0.95205    
-Precision:    
    Healthy: 1.00    
    High-Risk: 0.85    
-Recall:    
    Healthy: 0.99    
    High-Risk: 0.91    

## Summary
The Logistic Regression model performed very well in predicting healthy loans, achieving perfect precision for healthy loans and a high recall of 0.99. However, it incorrectly classified 10% of high-risk loans as healthy. Despite the model's high overall accuracy, this misclassification rate for high-risk loans is significant, as defaulted loans can lead to substantial financial losses.

The model's performance is influenced by the imbalance in the dataset, with relatively few high-risk loans compared to healthy loans. Increasing the proportion of high-risk loans in the training data or using techniques to handle imbalanced datasets could potentially improve the model's ability to identify high-risk loans accurately.

In loan classification, it is crucial to prevent high-risk loans from being misclassified as healthy, as the financial loss from a single defaulted loan can be greater than the interest gained from several healthy loans. Therefore, while the Logistic Regression model shows promise, further refinement and possibly exploring more complex models might be necessary to enhance the prediction of high-risk loans.

## Model Recommendation :   

Given the strong performance observed in the logistic regression model, I recommend deploying it for credit risk prediction. Its accuracy, along with balanced precision and recall scores, makes it a reliable tool for identifying both healthy and high-risk loans, enabling the company to make informed lending decisions and minimize the risk of default.
