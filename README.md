# 📞 Telecom Customer Churn Prediction — Logistic Regression

## 📌 Project Overview

This project uses **Logistic Regression** to predict whether a telecom customer is likely to **churn (leave)** or **stay**.

The goal is to identify customers who are likely to leave the company so that proactive retention offers can be provided.

---

## 🎯 Business Scenario

A telecom company is facing customer churn.

When a customer leaves:

- The company loses future revenue.
- The company spends additional money acquiring new customers.
- Early identification can help the company take retention actions.

The objective is to build a machine learning model that can:

- Estimate the probability of customer churn.
- Classify customers as **Likely to Churn** or **Likely to Stay**.
- Predict churn for unseen customers.
- Evaluate model performance.
- Understand the business impact of prediction errors.

---

## 📂 Dataset

**Dataset:** `WA_Fn-UseC_-Telco-Customer-Churn.csv`

| Property | Details |
|---|---|
| Rows | 7,043 |
| Columns | 21 |
| Target | Churn |
| Stay | 0 |
| Churn | 1 |

The `customerID` column was removed because it is only an identifier.

`TotalCharges` was converted from text to numeric format.

---

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- Jupyter Notebook

---
## 📊 Final Model Results

| Metric | Final Value |
|---|---:|
| Accuracy | **73.81%** |
| Precision | **50.43%** |
| Recall | **78.34%** |
| F1 Score | **61.36%** |
| ROC-AUC | **84.13%** |

### Confusion Matrix

|  | Predicted Stay | Predicted Churn |
|---|---:|---:|
| **Actual Stay** | 747 | 288 |
| **Actual Churn** | 81 | 293 |

### Key Business Results

- ✅ **293** actual churn customers correctly identified.
- ⚠️ **288** non-churn customers incorrectly flagged as churn.
- ❌ **81** actual churn customers were missed.
- ✅ **747** non-churn customers correctly identified.

### Final Conclusion

The Logistic Regression model achieved **73.81% accuracy**, **78.34% recall**, and **84.13% ROC-AUC**.

Since customer churn can result in direct revenue loss, **Recall is particularly important**. The model successfully identified **293 out of the actual churn customers in the test set**, while missing **81**.

The recommended next step is to **tune the classification threshold based on the business cost of retention offers versus losing customers**.

## 🔄 Machine Learning Workflow

```text
Telecom Customer Dataset
          ↓
Data Loading & Inspection
          ↓
Data Cleaning
          ↓
Feature Selection
          ↓
Train / Test Split
          ↓
Encoding & Scaling
          ↓
Logistic Regression
          ↓
Churn Probability
          ↓
Churn / Stay Classification
          ↓
Model Evaluation
          ↓
Business Interpretation
