# Churn_Prediction_Telco_Customer
This project is to predict the customers who are more likely to churn from the company based on customers who left within the last month labeled by "yes" or "no".
The dataset contains 7043 customers' info includes each customer's service with the company, their account information, and their demographic info. And the last column in the dataset is called "Churn" labeled "yes" or "no" whether that customer is a churner or not.

## Inspect and Cleaning the Data
For observing the data, we've found that the "TotalCharges" column is set as a obeject type but with numeric values. So the first step is to convert the data type from object to float type. Also from the deeper exploratory on the data, we also found that there are missing values in the "TotalCharges" column and the dataset is imbalanced. 

## Balancing the data by RandomOverSampler
We know this dataset is imbalanced. If we train and test with an imbalanced dataset, the result might be skewed. So we decided to use RandomOverSampler from imblearn to make the dataset balanced with same amount of "churns".
<img width="364" alt="imbalanced" src="https://user-images.githubusercontent.com/102785000/182012418-5ff1f343-a8a0-44a5-8499-f9dbd1f91ff4.png">
<img width="340" alt="balanced" src="https://user-images.githubusercontent.com/102785000/182012423-3633c30f-e0e2-42cf-92ee-8ea0ce5f86da.png">


## Feature Scaling
After using sklearn.metrics to import classification_report, confusion_matrix, ConfusionMatrixDisplayhen to train and test the model and gain the classification report, then we scale the 19 features by feature_importances. We can now see the scale of each feature effecting the churns. 

<img width="308" alt="feature_importance" src="https://user-images.githubusercontent.com/102785000/182012425-fbc8f162-46e5-4dee-a4b8-f21e2708c7c0.png"><img width="469" alt="feature_bar" src="https://user-images.githubusercontent.com/102785000/182012429-ff562557-66ee-44f4-ab8c-17f4b95491bc.png">
