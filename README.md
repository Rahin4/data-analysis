📊 End-to-End Customer Churn Prediction System
Overview

This project builds a complete machine learning pipeline to predict customer churn for a telecom company.

The objective is not only to classify churners but to translate predictions into business impact — retention strategy, lifetime value (LTV), and revenue protection.

Business Problem

Customer churn directly impacts revenue and growth.

From the dataset:

26.5% of customers churn

73.5% remain

Losing 1 in 4 customers creates high acquisition costs and unstable long-term growth.

This project answers:

Who is likely to churn?

Why are they leaving?

How can the business intervene?

Project Structure
customer-churn/
│
├── data/
│   ├── raw.csv
│   └── cleaned.csv
│
├── notebooks/
│   ├── 01_EDA.ipynb
│   ├── 02_Feature_Engineering.ipynb
│   ├── 03_Modeling.ipynb
│
├── app/
│   └── streamlit_app.py
│
├── models/
│   └── best_model.pkl
│
├── requirements.txt
└── README.md
Exploratory Data Analysis (EDA)

Key insights:

Customers with low tenure churn more.

Month-to-month contracts have the highest churn.

Higher monthly charges show stronger churn association.

Long-term contracts significantly reduce churn.

EDA included:

Distribution analysis

Correlation exploration

Tenure vs churn analysis

Contract type vs churn

Monthly charges vs churn

Data Preprocessing

Dropped non-predictive columns (e.g., customerID)

Converted Churn to binary (0/1)

Handled missing values

One-hot encoded categorical features

Verified all features numeric before modeling

Feature Engineering

Examples:

Tenure groups

Contract commitment indicators

Encoded service usage

Aggregated charge patterns

Focus: Improve model signal while keeping interpretability.

Models Implemented
1️⃣ Logistic Regression

Baseline model

Interpretable coefficients

Understand feature direction and impact

2️⃣ Tree-Based Models

Random Forest / Decision Tree

Captures nonlinear patterns

Better handling of feature interactions

Model Evaluation

Metrics used:

Accuracy

Precision / Recall

Confusion Matrix

ROC Curve

AUC Score

Why AUC?

Accuracy is misleading in imbalanced datasets.
AUC measures the model’s ability to separate churners from non-churners.
