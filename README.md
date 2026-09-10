# Customer Churn Prediction

## Overview

This project develops a machine learning model to predict customer churn using the Telco Customer Churn dataset.

## Objectives

- Explore customer churn patterns
- Perform data quality checks
- Select relevant features
- Preprocess numerical and categorical features
- Train Logistic Regression and Random Forest models
- Compare model performance
- Evaluate models using ROC-AUC
- Tune the classification threshold to improve churn detection

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
10. ROC-AUC Evaluation
11. Threshold Tuning
12. Final Model Evaluation

## Models

- Logistic Regression
- Random Forest

## Final Model

Logistic Regression was selected as the final model.

The classification threshold was set to 0.35, achieving the highest F1-score for the "Yes" class while also improving recall compared with the default threshold of 0.50.

## Final Results

For the "Yes" class:

- Precision: 0.56
- Recall: 0.72
- F1-score: 0.63

## Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- Jupyter