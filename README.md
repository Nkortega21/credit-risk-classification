# credit-risk-classification
UCI Data Analyst Module 20 - Supervised Learning Challenge

# Loan Default Prediction using Logistic Regression

## Overview of the Analysis

In this analysis, I applied a **Logistic Regression** model to predict whether loans would default or not based on financial data. The primary goal was to predict loan defaults using features from the dataset, which contains financial information about individuals seeking loans.

The dataset includes various financial details, but the target variable is whether the loan is likely to default (1) or not default (0). The dataset consists of **~20,000 samples**.

### Variables:
- **Target Variable (y):** `loan_status` – Whether the loan has a high risk of defaulting (1) or is healthy (0).
  - A value of **0** in the `loan_status` column means the loan is healthy (non-default).
  - A value of **1** means the loan has a high risk of defaulting.
- **Features (X):** Various financial metrics of the loan applicants (e.g., loan_size,	interest_rate,	borrower_income,	debt_to_income,	num_of_accounts,	derogatory_marks,	total_debt).

The task was to predict the likelihood of default (1) or non-default (0) based on these features. The model was trained using the **Logistic Regression** algorithm, a commonly used method for binary classification tasks.

### Stages of the Machine Learning Process:
1. **Data Preprocessing:** Data was cleaned and split into training and test sets.
2. **Model Selection:** Chose **Logistic Regression** as the model due to its simplicity and interpretability for binary classification.
3. **Model Evaluation:** Evaluated the model's performance using metrics like accuracy, precision, recall, f1-score, and a confusion matrix.

---

## Results

### Logistic Regression Model:

#### Confusion Matrix:
- **True Positives (TP):** 585
- **True Negatives (TN):** 18,658
- **False Positives (FP):** 107
- **False Negatives (FN):** 34

#### Classification Report:
- **Precision:**
  - Class 0 (Healthy Loan): 1.00
  - Class 1 (High Risk of Default): 0.85
- **Recall:**
  - Class 0 (Healthy Loan): 0.99
  - Class 1 (High Risk of Default): 0.95
- **F1-Score:**
  - Class 0 (Healthy Loan): 1.00
  - Class 1 (High Risk of Default): 0.89
- **Accuracy:** 99%
- **Macro Average:**
  - Precision: 0.92
  - Recall: 0.97
  - F1-Score: 0.94
- **Weighted Average:**
  - Precision: 0.99
  - Recall: 0.99
  - F1-Score: 0.99

---

## Summary

### Which Model Performed Best?
The **Logistic Regression** model performed excellently, achieving **99% accuracy**, indicating that it correctly predicted most outcomes. It also exhibited high **recall** for identifying loans with a high risk of default (95%), which is crucial in financial applications where missing high-risk loans can lead to significant financial loss.

### Does Performance Depend on the Problem?
Yes, performance is dependent on the problem being solved. In this case, predicting **high-risk loans** (class 1) is more important than predicting **healthy loans** (class 0), since failing to predict a high-risk loan may result in financial loss. The model performed better at identifying healthy loans but still did well with high-risk loans, with a **recall of 95%** for class 1. However, the **precision for class 1** (85%) indicates that some healthy loans were incorrectly predicted as high-risk loans.
