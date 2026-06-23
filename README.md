# Customer Churn Prediction

## Overview
Customer churn is a major challenge for subscription-based businesses because losing existing customers is often more expensive than acquiring new ones. This project aims to predict whether a customer is likely to churn based on demographic information, account details, and the services they use.

The project includes data cleaning, exploratory data analysis (EDA), feature engineering, model training, evaluation, and prediction for new customers using a saved machine learning model.

---

## Dataset
The dataset contains comprehensive customer profiles, including:
* **Customer Demographics:** Age, gender, and partner/dependent status.
* **Account Information:** Contract type, payment method, paperless billing, and tenure.
* **Services Subscribed:** Phone, internet, online security, tech support, streaming TV, etc.
* **Financial Metrics:** Monthly charges and total charges.
* **Target Variable:** `Churn` (Yes / No).

---

## Project Workflow

### 1. Data Cleaning
* Checked for and handled missing values.
* Converted data types where necessary (e.g., ensuring total charges are numeric).
* Removed unnecessary inconsistencies across features.

### 2. Exploratory Data Analysis (EDA)
Performed exploratory analysis to understand customer behavior and identify key drivers of churn. Key observations include:
* **Contract Type:** Customers with month-to-month contracts tend to churn more frequently than those with long-term contracts.
* **Tenure:** Customers with shorter tenure are significantly more likely to leave.
* **Charges:** Higher monthly charges are heavily associated with increased churn.
* **Tech Support & Security:** Customers using additional support and security services generally exhibit lower churn rates.

*Visualizations used:* Count plots, histograms, distribution plots, and a correlation heatmap.

### 3. Data Preprocessing & Feature Engineering
* Label encoded and one-hot encoded categorical variables.
* Handled class imbalance using **SMOTE** (Synthetic Minority Over-sampling Technique).
* Split the data into stratified training and testing sets.

---

## Models Used
Three machine learning models were trained and compared:
1. **Decision Tree Classifier**
2. **Random Forest Classifier**
3. **XGBoost Classifier**

Among these, the **Random Forest Classifier** produced the best overall performance and was selected as the final production model.

---

## Model Evaluation
The models were evaluated using multiple performance metrics to ensure robustness:
* Accuracy Score
* Confusion Matrix
* Classification Report (Precision, Recall, F1-Score)
* ROC-AUC Curve

The Random Forest model achieved the optimal balance between overall accuracy and minority-class recall performance.

---

## Model Deployment & Saving
The final Random Forest model was serialized and saved as a `pickle` file along with the necessary feature names so it can be reused without retraining. 

The project repository includes scripts to demonstrate how to:
* Load the saved model artifact.
* Pipeline and preprocess data for a new customer.
* Predict whether the customer is likely to churn.

---

## Technologies Used
* **Languages:** Python
* **Data Libraries:** Pandas, NumPy
* **Visualization:** Matplotlib, Seaborn
* **Machine Learning:** Scikit-learn, XGBoost
* **Imbalance Handling:** imbalanced-learn (SMOTE)
* **Model Serialization:** Pickle

---

## Conclusion
This project demonstrates an end-to-end machine learning workflow, starting from raw customer data and ending with churn prediction for unseen customers. By comparing multiple models and selecting the best-performing one, the project highlights how machine learning can help businesses identify customers at risk of leaving and proactively support better customer retention strategies.
