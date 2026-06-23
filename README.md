# customer-churn-prediction
## Overview

Customer churn is a major challenge for subscription-based businesses because losing existing customers is often more expensive than acquiring new ones. This project aims to predict whether a customer is likely to churn based on demographic information, account details, and the services they use.
The project includes data cleaning, exploratory data analysis (EDA), feature engineering, model training, evaluation, and prediction for new customers using a saved machine learning model.
---
## Dataset

The dataset contains customer information such as:
•	Customer demographics
•	Account information
•	Services subscribed
•	Monthly and total charges
•	Churn status (Target Variable)
Target variable:
•	Churn
o	Yes
o	No
---
## Project Workflow

1. Data Cleaning
•	Checked for missing values
•	Converted data types where necessary
•	Removed unnecessary inconsistencies

2. Exploratory Data Analysis (EDA)
Performed exploratory analysis to understand customer behavior and identify patterns related to churn.
Some observations include:
•	Customers with month-to-month contracts tend to churn more frequently.
•	Customers with shorter tenure are more likely to leave.
•	Higher monthly charges are associated with increased churn.
•	Customers using additional support and security services generally have lower churn rates.
Visualizations used include:
•	Count plots
•	Histograms
•	Correlation heatmap
•	Distribution plots

3. Data Preprocessing
•	Label encoded categorical features
•	Balanced the dataset using SMOTE
•	Split the data into training and testing sets
---
## Models Used

Three machine learning models were trained and compared:
•	Decision Tree Classifier
•	Random Forest Classifier
•	XGBoost Classifier
Among these, Random Forest produced the best overall performance and was selected as the final model.
---
## Model Evaluation

The models were evaluated using:
•	Accuracy Score
•	Confusion Matrix
•	Classification Report
•	ROC-AUC Curve
The Random Forest model achieved the best balance between accuracy and classification performance.
---
## Model Saving

The final Random Forest model was saved as a pickle file along with the feature names so it can be reused without retraining.
The project also demonstrates how to:
•	Load the saved model
•	Prepare data for a new customer
•	Predict whether the customer is likely to churn
---
## Technologies Used
•	Python
•	Pandas
•	NumPy
•	Matplotlib
•	Seaborn
•	Scikit-learn
•	XGBoost
•	imbalanced-learn (SMOTE)
•	Pickle
---
## Conclusion
This project demonstrates an end-to-end machine learning workflow, starting from raw customer data and ending with churn prediction for unseen customers. By comparing multiple models and selecting the best-performing one, the project highlights how machine learning can help businesses identify customers at risk of leaving and support better customer retention strategies.
