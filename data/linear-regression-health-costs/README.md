# Health Insurance Cost Prediction with Linear Regression

This project uses linear regression models to predict medical insurance charges based on personal and lifestyle attributes such as age, sex, BMI, number of children, and smoking status. The dataset is commonly used for regression tasks and highlights the importance of feature relationships, encoding, scaling, and model selection in a real-world predictive scenario.

 **CRISP-DM Alignment:**  
This notebook corresponds to the **Modeling** phase of the CRISP-DM methodology. It is part of a series of independent exercises, each focused on a different stage of the process using distinct datasets.

## Objective

To build a regression model capable of estimating medical costs, evaluate the model's performance, and test how different preprocessing and model configurations affect results.

##  Dataset

The dataset includes the following attributes for each individual:

- Age, sex, BMI
- Number of children
- Smoker status
- Region (not used in this analysis)
- Charges (target variable)

Source: Open dataset used for educational purposes (commonly available on Kaggle and ML tutorials)

## Workflow Summary

- Data inspection and visualization
- Outlier detection and capping
- Correlation analysis
- Train/test split with stratification by smoker
- Preprocessing pipelines (scaling and encoding)
- Model training and R² evaluation
- Comparison of polynomial models (degrees 1 to 5)

## Key Insights

- Smoking has a strong influence on charges.
- Polynomial regression of degree 2 yielded the best R² score.
- Feature scaling and encoding significantly affect model performance.

##  Tools Used

- Python
- Pandas, NumPy
- Seaborn, Matplotlib
- Scikit-learn

## Files

- `insurance_cost_regression.ipynb`: Notebook with full analysis and modeling
- `insurance.csv`: Dataset used (public educational data)

## Contact

Feel free to reach out if you have any questions or suggestions!
