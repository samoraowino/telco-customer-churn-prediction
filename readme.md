# Telco Customer Churn Prediction

This project aims to predict whether a telecom customer will churn (leave the service) using historical data. 

---

##  Project Objective

Telecom companies lose significant revenue when customers leave. This project uses customer account and usage data to build a classification model that predicts the likelihood of churn. The model helps identify high-risk customers so that proactive retention strategies can be applied.

---

##  Dataset Overview

- **Source**: [Kaggle – Telco Customer Churn](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)
- **Size**: 7,043 customer records
- **Target Variable**: `Churn` (Yes = customer left, No = customer stayed)
- **Key Features**: `tenure`, `MonthlyCharges`, `Contract`, `InternetService`, and `PaymentMethod`

---

##  Project Workflow

### 1. Data Understanding
- Explored dataset structure and feature types
- Identified target and supporting variables

### 2. Data Cleaning & Preprocessing
- Converted `TotalCharges` to numeric and dropped missing values
- Removed duplicates and irrelevant columns (like `customerID`)
- Encoded categorical variables using one-hot encoding

### 3. Exploratory Data Analysis (EDA)
- Visualized churn distribution
- Correlation heatmap to identify strong predictors
- Compared churn rates across contract types

### 4. Model Development
- Split data into training and test sets (80/20)
- Trained a **Decision Tree Classifier** (depth = 5)
- Evaluated using accuracy, precision, recall, and classification report

### 5. Feature Importance
- Identified `tenure`, `MonthlyCharges`, and `Contract_Two year` as the top churn predictors

---

##  Results

- **Model Accuracy**: 79%
- **Key Insight**: Short-tenure customers on month-to-month contracts are most likely to churn
- **Business Use**: Helps telecom companies target at-risk customers with better offers

---

## Ethical, Privacy & Data Security Considerations

We addressed concerns such as:
- **Privacy**: Removed identifiers and minimized data use
- **Security**: Recommended encryption and access controls
- **Ethics**: Proposed transparency, informed consent, and fairness audits
- **Compliance**: Aligned with the **Kenya Data Protection Act** and global best practices

Details included in the final notebook.

---

##  Tools Used

- Python
- Pandas, NumPy
- Seaborn, Matplotlib
- scikit-learn