# Improved Fraud Detection for E-commerce and Banking Transactions

## Project Overview

Fraudulent activities pose a significant risk to both e-commerce platforms and financial institutions. This project focuses on developing robust, accurate, and explainable machine learning models to detect fraudulent transactions in two different domains:

- **E-commerce transactions**
- **Bank credit card transactions**

The project is conducted in the context of **Adey Innovations Inc.**, a fintech company aiming to improve transaction security while maintaining a smooth customer experience.

A major challenge addressed in this work is **extreme class imbalance**, where fraudulent transactions represent only a very small fraction of all transactions. Special care is taken in feature engineering, model evaluation, and interpretation to ensure reliable fraud detection.

---

## Business Objective

The primary business objective is to **maximize fraud detection accuracy while minimizing false positives**.

- **False Positives** (legitimate transactions flagged as fraud) harm customer experience and trust.
- **False Negatives** (missed fraud cases) result in direct financial losses.

This project balances these competing costs by:

- Using evaluation metrics suitable for imbalanced data
- Applying resampling techniques only where appropriate
- Prioritizing interpretability for business decision-making

---

## Datasets Used

### 1. E-commerce Fraud Dataset (`Fraud_Data.csv`)

Contains user-level and transaction-level information such as:

- User demographics
- Signup and purchase timestamps
- Transaction values
- Device, browser, and traffic source
- IP address information
- Fraud label (`class`)

### 2. IP Address to Country Mapping (`IpAddress_to_Country.csv`)

Maps IP address ranges to their corresponding countries.  
Used to enhance fraud detection through **geolocation analysis**.

### 3. Credit Card Transactions Dataset (`creditcard.csv`)

A highly imbalanced dataset of bank transactions with:

- PCA-transformed anonymized features (V1–V28)
- Transaction amount
- Time-based feature
- Fraud label (`Class`)

---

## Project Scope and Methodology

### 1. Data Analysis and Preprocessing

- Data cleaning and type correction
- Removal of duplicates
- Exploratory Data Analysis (EDA)
- Class imbalance analysis
- IP address to country mapping
- Time-based and behavioral feature engineering

### 2. Feature Engineering

Key engineered features include:

- Time since signup
- Hour of day and day of week
- Transaction frequency and velocity
- Geolocation-based risk indicators

### 3. Handling Class Imbalance

- Stratified train-test splitting
- Application of SMOTE on training data only
- Justification of resampling strategy based on business impact

### 4. Model Development

- Baseline Logistic Regression model
- Ensemble models (Random Forest / Gradient Boosting)
- Hyperparameter tuning
- Stratified cross-validation

### 5. Model Evaluation

Models are evaluated using:

- Precision-Recall AUC (AUC-PR)
- F1-score
- Confusion matrix

Accuracy is intentionally avoided as a primary metric due to extreme class imbalance.

### 6. Model Explainability (XAI)

- Feature importance analysis
- SHAP summary plots
- Local explanations for individual predictions:
  - True Positive
  - False Positive
  - False Negative

Explainability is used to derive actionable business insights.

---

## Key Outcomes

- Improved fraud detection performance on imbalanced datasets
- Clear understanding of fraud drivers such as:
  - Transaction timing
  - Velocity patterns
  - Geolocation risk
- Interpretable models suitable for real-world deployment

---

## Business Impact

This project enables organizations to:

- Detect fraud more accurately in real time
- Reduce financial losses
- Improve customer trust
- Support compliance and audit requirements through explainable AI

---

## Tools and Technologies

- Python
- pandas, NumPy
- scikit-learn
- imbalanced-learn
- SHAP
- Matplotlib, Seaborn

---

## Evaluation Criteria Alignment

This project demonstrates:

- Strong technical implementation
- Business-oriented problem solving
- Clear communication of complex analytical results
- Professional and reproducible machine learning workflow

---

## Authors & Acknowledgment

Developed as part of a fraud detection challenge under the guidance of tutors from Adey Innovations Inc.
