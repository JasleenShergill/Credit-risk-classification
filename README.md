****📚 Credit Risk Analysis****

Welcome to the Credit Risk Analysis project! 🎉 This project aims to predict the risk status of loans using a logistic regression model. Below you'll find the steps taken to prepare the data, build the model, evaluate its performance, and the results obtained.

**🚀 Getting Started**

Data Preparation

**Read the Data:** The dataset lending_data.csv is read into a Pandas DataFrame.
Create Labels and Features:
**Labels (y):** The loan_status column (0: healthy loan, 1: high-risk loan).
**Features (x):** All other columns except loan_status.
Split the Data: Split the data into training and testing datasets using train_test_split.

**📊 Results**

**Confusion Matrix**:  

![alt text](image-1.png)]

Classification Report:

![alt text](image.png)

**Performance Metrics**
Accuracy: 94%
 Precision:
 Healthy loans (0): 100%
 High-risk loans (1): 89%
 
**Recall:**
 Healthy loans (0): 100%
 High-risk loans (1): 87%

 ## Summary
The Logistic Regression model performed very well in predicting healthy loans, achieving perfect precision for healthy loans and a high recall of 0.99. However, it incorrectly classified 10% of high-risk loans as healthy. Despite the model's high overall accuracy, this misclassification rate for high-risk loans is significant, as defaulted loans can lead to substantial financial losses.

The model's performance is influenced by the imbalance in the dataset, with relatively few high-risk loans compared to healthy loans. Increasing the proportion of high-risk loans in the training data or using techniques to handle imbalanced datasets could potentially improve the model's ability to identify high-risk loans accurately.

In loan classification, it is crucial to prevent high-risk loans from being misclassified as healthy, as the financial loss from a single defaulted loan can be greater than the interest gained from several healthy loans. Therefore, while the Logistic Regression model shows promise, further refinement and possibly exploring more complex models might be necessary to enhance the prediction of high-risk loans.

## Model Recommendation :   

Given the strong performance observed in the logistic regression model, I recommend deploying it for credit risk prediction. Its accuracy, along with balanced precision and recall scores, makes it a reliable tool for identifying both healthy and high-risk loans, enabling the company to make informed lending decisions and minimize the risk of default.

