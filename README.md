# Customer Churn Prediction

## Overview

This project develops a machine learning model to predict customer churn using the Telco Customer Churn dataset.

The goal is to identify customers who are likely to churn and evaluate different modeling approaches with a focus on improving churn detection.

## Objectives

* Explore customer churn patterns
* Perform data quality checks
* Identify relevant features
* Preprocess numerical and categorical features
* Train Logistic Regression and Random Forest models
* Compare model performance
* Evaluate the models using classification metrics
* Apply cross-validation
* Tune the classification threshold to improve churn detection

## Dataset

The project uses the **Telco Customer Churn** dataset, which contains information about customer services, contract types, tenure, and billing.

The dataset contains **7,043 customer records**.

## Machine Learning Workflow

1. Data Exploration
2. Data Quality Checks
3. Exploratory Data Analysis
4. Feature Selection
5. Train-Test Split
6. Data Preprocessing
7. Model Training
8. Cross-Validation
9. Model Comparison
10. Threshold Tuning
11. Final Model Evaluation

## Key Findings

The exploratory analysis showed several patterns associated with higher churn:

* Month-to-month contracts have substantially higher churn than longer-term contracts.
* Customers with shorter tenure tend to have higher churn rates.
* Higher monthly charges are associated with increased churn.
* Fiber optic customers showed higher churn compared with some other internet service categories.
* Electronic check customers showed higher churn than other payment methods.

## Preprocessing

The preprocessing pipeline includes:

* Converting `Total Charges` to numeric values
* Separating numerical and categorical features
* Standardizing numerical features using `StandardScaler`
* Encoding categorical features using `OneHotEncoder`
* Handling unseen categorical values with `handle_unknown="ignore"`

## Models

Two classification models were evaluated:

* Logistic Regression
* Random Forest

### Model Comparison

Logistic Regression achieved higher overall performance for the churn detection task.

Random Forest achieved an accuracy of approximately **79.3%**, while Logistic Regression achieved approximately **80.2%** at the default threshold.

Because detecting customers who are likely to churn is important for this problem, additional attention was given to **recall and F1-score for the "Yes" class** rather than accuracy alone.

## Threshold Tuning

The default classification threshold of `0.50` was adjusted to `0.35`.

A lower threshold increases the number of customers classified as likely to churn, improving the model's ability to detect actual churn cases.

The final threshold of **0.35** provided a better balance between precision and recall for the churn class.

## Final Model

**Logistic Regression** was selected as the final model.

The final classification threshold was set to **0.35** to improve churn detection compared with the default threshold of `0.50`.

### Final Results

For the **"Yes" (Churn)** class at a threshold of `0.35`:

* Precision: **0.56**
* Recall: **0.72**
* F1-score: **0.63**

The model successfully identifies a larger proportion of customers who actually churn compared with using the default threshold.

## Cross-Validation

The Logistic Regression model achieved the following F1-scores across 5 cross-validation folds:

* 0.774
* 0.746
* 0.746
* 0.741
* 0.735

**Mean CV F1-score: 0.748**

## Technologies

* Python
* Pandas
* NumPy
* Matplotlib
* Scikit-learn
* Jupyter Notebook

## Project Structure

```text
customer-churn-ml/
│
├── data/
│   └── Telco_customer_churn.xlsx
│
├── notebooks/
│   └── 01_churn_prediction.ipynb
│
├── src/
├── models/
├── app/
│
├── .gitignore
├── README.md
└── requirements.txt
```


