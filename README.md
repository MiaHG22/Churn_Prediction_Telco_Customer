# Churn_Prediction_Telco_Customer
This project is to predict the customers who are more likely to churn from the company based on customers who left within the last month labeled by "yes" or "no".
The dataset contains 7043 customers' info includes each customer's service with the company, their account information, and their demographic info. And the last column in the dataset is called "Churn" labeled "yes" or "no" whether that customer is a churner or not.

## Inspect and Cleaning the Data
For observing the data, we've found that the "TotalCharges" column is set as a obeject type but with numeric values. So the first step is to convert the data type from object to float type. Also from the deeper exploratory on the data, we also found that there are missing values in the "TotalCharges" column and the dataset is imbalanced. 

## Balancing the data by RandomOverSampler
We know this dataset is imbalanced. If we train and test with an imbalanced dataset, the result might be skewed. So we decided to use RandomOverSampler from imblearn to make the dataset balanced with same amount of "churns".



## Feature Scaling
After using sklearn.metrics to import classification_report, confusion_matrix, ConfusionMatrixDisplayhen to train and test the model and gain the classification report, then we scale the 19 features by feature_importances. We can now see the scale of each feature effecting the churns. 

