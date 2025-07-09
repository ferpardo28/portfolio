# Credit Risk EDA

This project contains an exploratory data analysis (EDA) on a dataset related to loan applications and credit risk.

## 📌 Objective

To explore patterns and relationships in loan applicant data that may be associated with credit default risk. The goal is to support future modeling tasks by understanding variable distributions, correlations, and data quality.

## 🗂️ Dataset

The dataset includes both numerical and categorical features related to:

- Applicant's age, income, and debt
- Loan characteristics (intent, grade, interest rate)
- Credit history (past defaults, credit balances)

**Target variable:** `loan_status` (1 = defaulted, 0 = not defaulted)

## 🔍 Analysis Performed

- Inspection of data structure and types
- Missing values and descriptive statistics
- Distribution plots (histograms, boxplots)
- Outlier detection using IQR
- Categorical variable distributions
- Correlation heatmap
- Comparison of features by loan status

## 📊 Key Insights

- Applicants with higher `loan_percent_income` or `loan_int_rate` have higher default risk
- Specific loan intents and credit grades are more common among defaulters
- Several numerical variables are right-skewed and contain outliers

## 🛠️ Tools Used

- Python
- Pandas, NumPy
- Seaborn, Matplotlib

## 📁 Files

- `credit_risk_eda.ipynb`: Jupyter notebook with the full analysis
- `credit_risk_dataset.csv`: Dataset used 

## 📬 Contact

Feel free to reach out if you have questions or feedback!
