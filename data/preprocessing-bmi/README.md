
# Data Preprocessing and BMI Analysis

This project focuses on data preparation techniques applied to a survey dataset with both numerical and categorical variables. The goal is to clean and enrich the dataset to support further analysis or modeling efforts.

 **CRISP-DM Alignment:**  
This notebook demonstrates the **Data Preparation** stage of the CRISP-DM methodology using an independent dataset.

---

## Objective

- Clean and explore data from a health-related survey
- Handle missing values and outliers
- Create a new feature (BMI) based on weight and height
- Analyze relationships between BMI and categorical variables

---

##  Dataset

The dataset (`responses.csv`) includes:

- Demographic and personal characteristics of survey participants
- Variables such as `Weight`, `Height`, `Education`, `Gender`, etc.

> This dataset was provided as part of an academic exercise. No personal or sensitive information is included.

---

## Analysis Performed

- Data inspection: structure, types, summary statistics
- Handling missing values with visual diagnostics and statistical tests
- Outlier detection and removal using the IQR method for `Weight`, `Height`, and `BMI`
- Feature engineering: BMI = weight / height²
- Exploratory analysis of BMI by categorical attributes

---

## Key Insights

- The BMI feature shows strong right skewness and significant outliers that were removed
- Education level appears related to BMI: participants with doctoral degrees tend to have higher BMI
- Imputation with the median and IQR-based filtering improved data quality significantly

---

##  Tools Used

- Python
- Pandas, NumPy
- Seaborn, Matplotlib
- Scipy (for t-test and chi-squared test)

---

## Files

- `preprocessing_bmi_survey.ipynb`: Jupyter notebook with all analysis and code
- `responses.csv`: Cleaned dataset used in this notebook

---

## Contact

For questions or suggestions, feel free to reach out via GitHub or email.
