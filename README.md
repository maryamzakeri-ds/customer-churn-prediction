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
4. Feature Engineering 
5. Data Preprocessing 
6. Model Training 
7. Model Evaluation 
8. Hyperparameter Tuning 
9. Feature Importance Analysis
10. Model Deployment Preparation

---

## Data Cleaning

* Removed `customerID`
* Converted `TotalCharges` to numeric values
* Handled missing values

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
* Random Forest (Balanced)
* XGBoost

Hyperparameter tuning was performed using **GridSearchCV**.

---

## Model Performance

| Model                     | Accuracy | Precision |   Recall | F1-score |
| ------------------------- | -------: | --------: | -------: | -------: |
| Logistic Regression       |     0.81 |      0.66 |     0.56 |     0.60 |
| Decision Tree             |     0.72 |      0.47 |     0.48 |     0.47 |
| Random Forest             |     0.78 |      0.61 |     0.49 |     0.54 |
| Random Forest (Balanced)  |     0.77 |      0.55 |     0.62 |     0.58 |
| Tuned Logistic Regression |     0.74 |      0.51 | **0.79** | **0.62** |
| Tuned Random Forest       |     0.76 |      0.53 |     0.76 | **0.62** |
| XGBoost                   |     0.78 |      0.59 |     0.52 |     0.55 |

---

## Key Insights

The most influential features identified by the models include:

* Customer tenure
* Contract type
* Total charges

Customers with longer tenure and long-term contracts were significantly less likely to churn, while customers with month-to-month contracts showed a much higher churn risk.

---

## Technologies

* Python
* Pandas
* NumPy
* Matplotlib
* Scikit-learn
* XGBoost
* Joblib

---

## Model Deployment

The final trained model was saved using **Joblib** and successfully loaded to perform predictions on new customer data.

---

## Conclusion

This project demonstrates an end-to-end machine learning workflow for customer churn prediction, from data exploration and preprocessing to model selection, evaluation, interpretation, and inference.

The resulting model can help businesses identify customers at risk of churn and support data-driven customer retention strategies.
