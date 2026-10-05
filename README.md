# Customer Churn Prediction

## Project Overview

Customer churn prediction is an important business problem that helps companies identify customers who are likely to leave their service. Early identification enables businesses to implement retention strategies and reduce customer loss.

In this project, multiple machine learning models were developed and compared to predict customer churn using the Telco Customer Churn dataset.

---

## Dataset

* **Dataset:** Telco Customer Churn
* **Target Variable:** `Churn`
* **Task:** Binary Classification

The dataset contains customer demographic information, subscribed services, account information, and billing details.

---

## Project Workflow

1. Data Understanding
2. Data Cleaning 
3. Exploratory Data Analysis (EDA)
4. Data Preprocessing 
5. Model Training 
6. Model Evaluation 
7. Hyperparameter Tuning 
8. Feature Importance Analysis

---

## Data Cleaning

* Removed `customerID`
* Converted `TotalCharges` to numeric values
* Handled missing values
* Split Dataset into Training and Test Sets

## Data Preprocessing

* One-Hot Encoding for categorical variables
* Standard Scaling for numerical variables
* Built preprocessing pipeline using `ColumnTransformer`

---

## Models

The following models were trained and evaluated:

* Logistic Regression
* Decision Tree
* Random Forest
* XGBoost

Hyperparameter tuning was performed using **GridSearchCV** and **RandomizedSearchCV**.

---

## Model Performance

| Model                     | Accuracy | Precision |   Recall | F1-score | False Negative | AUC |
| ------------------------- | -------: | --------: | -------: | -------: | -------------: | --: |
| Logistic Regression       |     0.81 |      0.66 |     0.56 |     0.60 |            165 |  84 |
| Decision Tree             |     0.73 |      0.49 |     0.50 |     0.49 |            187 |  65 |
| Random Forest             |     0.79 |      0.62 |     0.49 |     0.55 |            192 |  81 | 
| XGBoost                   |     0.78 |      0.59 |     0.52 |     0.55 |            180 |  82 |
| Tuned Logistic Regression |     0.74 |      0.50 | **0.79** | **0.62** |         **79** |  84 |
| Tuned XGBoost             |     0.81 |      0.67 |     0.53 |     0.59 |            175 |  84 |


---

## Key Insights

The most influential features identified by the models include:

* Contract type
* Customer tenure

Customers with longer tenure and long-term contracts were significantly less likely to churn, while customers with month-to-month contracts showed a much higher churn risk.

---

## Technologies

* Python
* Pandas
* NumPy
* Matplotlib
* Scikit-learn
* XGBoost

---

## Conclusion

This project demonstrates an end-to-end machine learning workflow for customer churn prediction, from data exploration and preprocessing to model selection, evaluation, interpretation, and inference.

The resulting model can help businesses identify customers at risk of churn and support data-driven customer retention strategies.
