# Loan Default Risk Analysis

## 📌 Project Overview

Loan default is a significant issue in the finance industry, costing billions annually.
This project aims to build a **predictive model** that identifies high-risk borrowers and recommends **data-driven strategies** to minimize loan defaults.

## Business Objectives

- Identify key factors influencing loan defaults.
- Predict default risk using machine learning models.
- Recommend approval strategies for financial institutions.

## Tech Stack

- **Python** (Pandas, Scikit-learn, Matplotlib, Seaborn)
- **SQL** (for data extraction and querying)
- **Power BI/Tableau** (for interactive dashboards)
- **Jupyter Notebook** (for EDA and modeling)
- **GitHub Actions** (for workflow automation)

## 📂 Project Structure

- `data/` – Source data files (cleaned datasets are stored here)
- `notebooks/` – Jupyter notebooks for EDA and ML models
- `reports/` – Business insights and final recommendations
- `src/` – Python scripts for data processing and model training
- `dashboards/` – Power BI or Tableau dashboards

## EDA - Exploratory Data Analysis

### Distribution of Credit Limits

- Most customers have credit limits **below $200,000**, with a **right-skewed distribution**.
- Higher credit limits may indicate **lower risk**, while low credit customers may have **higher default rates**.
  ![Credit Limit Distribution](images/Distribution_of_Credit_Limits.png)

### Repayment Status Over Time

- Customers with **delayed payments in earlier months** tend to continue **defaulting**.
- Many **outliers (dots)** represent **chronic late payers**, indicating **high-risk borrowers**.
- Financial institutions should **intervene early** when a customer **misses a payment**.
  ![Repayment Status Over Time](images/Payment_Behavior_Over_Time.png)

## Model Performance & Comparisons

### **Logistic Regression Results**

| Metric    | Score |
| --------- | ----- |
| Precision | 0.93  |
| Recall    | 0.95  |
| F1-Score  | 0.94  |
| Accuracy  | 0.89  |

- **Logistic Regression performed well** but struggled with recall for high-risk borrowers.
- **Best Parameters:** `{'C': 0.001, 'solver': 'lbfgs'}`

### **Random Forest with SMOTE**

| Metric    | Score |
| --------- | ----- |
| Precision | 0.97  |
| Recall    | 0.91  |
| F1-Score  | 0.94  |
| Accuracy  | 0.90  |

- **SMOTE (Synthetic Minority Over-sampling Technique) improved recall** for high-risk borrowers.
- Random Forest achieved a better balance of **precision and recall** compared to Logistic Regression.

## 🔍 Key Insights

- **SMOTE improved the model's ability to detect high-risk borrowers** by increasing recall.
- **Random Forest performed better overall**, making it the preferred model for this use case.
- **Future Work:** Fine-tuning hyperparameters and exploring additional models like XGBoost.

## 👥 Contributors

- **Philip Timothe** – Business Analyst & Project Lead
