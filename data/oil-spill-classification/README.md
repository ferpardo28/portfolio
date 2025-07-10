# Oil Spill Classification with Logistic Models and Resampling

This notebook demonstrates a complete supervised learning pipeline for a highly imbalanced binary classification problem: detecting oil spills from remote sensing image features.

The project follows a classic machine learning workflow:
- Data cleaning and preparation
- Feature transformation
- Model training with cross-validation
- Evaluation using appropriate metrics for imbalanced datasets
- Hyperparameter tuning and resampling

## Dataset

The dataset (`oil_spill.csv`) contains 1,000 observations and 49 features extracted from satellite images. Only **4.4% of samples belong to the positive class**, which corresponds to actual oil spills.  
Place the dataset in the same folder as the notebook before running it.

## Objective

Classify whether a given image patch corresponds to an oil spill (`1`) or not (`0`) using logistic-based classifiers and strategies to handle class imbalance.

## Models Evaluated

1. **DummyClassifier** – baseline
2. **Logistic Regression (LR)** – no penalty, L1, L2, Elastic Net
3. **k-Nearest Neighbors (kNN)**  
4. **Balanced Versions** of the above using `class_weight='balanced'`
5. **Best Model** – Logistic Regression with L2, tuned via GridSearchCV + `SMOTETomek`

## Evaluation Strategy

- **RepeatedStratifiedKFold** cross-validation
- **G-Mean** used as the main evaluation metric  
- Also reported: Accuracy, ROC Curve, Precision-Recall Curve, Confusion Matrix

**Why G-Mean?**  
G-Mean evaluates the balance between sensitivity and specificity, making it more appropriate for imbalanced datasets.

## Results

- The **best model** (Logistic Regression with L2 + SMOTETomek) achieved:
  - **G-Mean (test)**: 0.596
  - **PR-AUC (test)**: 0.36

Despite resampling and tuning, performance remained limited due to:
- Small dataset size (only 1,000 samples)
- Extremely low representation of the positive class (≈44 examples)

## Limitations

- The model performs similarly to the baseline DummyClassifier.
- Most classifiers struggled to generalize to the positive class.
- Oversampling helped marginally, but a larger and more balanced dataset is likely needed.

---

**Note:**  
This notebook was created as part of a university course on Artificial Intelligence and Machine Learning. It represents an academic exercise within a CRISP-DM-like process, using a small, real-world dataset.
