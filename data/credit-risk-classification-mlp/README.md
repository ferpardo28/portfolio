# Credit Risk Classification Using MLP and Imbalanced-Learn Techniques

This notebook performs credit risk classification using the South German Credit dataset. It applies data preprocessing, class imbalance handling, and multiple classification models, culminating in the evaluation and selection of the best-performing model (MLP).

## 🧰 Setup

Before running the notebook, install the required packages:

```bash
!pip install scikit-learn==1.5.0
!pip install -U imbalanced-learn
```

## 🧪 Project Structure

This project follows the CRISP-DM methodology, including the following stages:

- Data loading and exploratory analysis
- Class imbalance inspection and correction using SMOTETomek and other methods
- Data transformation pipelines for numeric, ordinal, and nominal features
- Cross-validation with multiple classifiers (Logistic Regression, KNN, Decision Tree, Random Forest, XGBoost, MLP, SVM)
- Evaluation with metrics like Accuracy, Precision, Recall, F1, AUC, G-Mean
- Feature importance and final model interpretation

## 📊 Best Model

The best-performing model was an MLP (Multi-layer Perceptron) with SMOTETomek. It achieved the highest F1 and balanced performance between recall and precision, making it suitable for identifying risky loan applicants while minimizing false rejections.

## 📁 Notes

- The data is loaded from Google Drive. Update the path accordingly if using a different environment.
- All code is structured for clarity and reproducibility, including docstrings and comments in English.

---

This notebook was developed as part of an academic exercise and does not use real financial data.
