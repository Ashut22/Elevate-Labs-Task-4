# Breast Cancer Diagnosis using Logistic Regression

## Overview
This task applies logistic regression to the Breast Cancer Wisconsin (Diagnostic) dataset to classify tumors as malignant or benign based on digitized image features. The workflow includes data preprocessing, exploratory data analysis, model training, evaluation, and threshold tuning.

## Dataset
- **Samples:** 569
- **Features:** 30 numeric features (after removing ID and null columns)
- **Target:** Diagnosis (`M` = malignant, `B` = benign), encoded as 1 and 0 respectively.

## Steps

### Data Preprocessing
- Removed `id` and `Unnamed: 32` columns (non-predictive or empty).
- Encoded diagnosis labels to binary (Malignant=1, Benign=0).
- Scaled features using `StandardScaler` for better model performance.

### Exploratory Data Analysis
- Visualized class distribution using a count plot.
- Computed and visualized feature correlation matrix using a heatmap to identify relationships and redundant features.

### Model Building
- Split data into training (80%) and testing (20%) sets with stratification.
- Trained a logistic regression classifier on scaled features.
- Predicted tumor classes and probabilities on the test set.

### Evaluation Metrics
- **Confusion Matrix**: Summarizes true/false positives and negatives.
- **Precision**: 0.9750 — proportion of correctly predicted malignant cases.
- **Recall**: 0.9286 — proportion of actual malignant cases detected.
- **ROC-AUC**: 0.9960 — overall ability to distinguish classes.
- Plotted ROC curve for visual performance analysis.

### Threshold Tuning
- Adjusted classification threshold from default 0.5 to 0.3.
- Improved recall while maintaining high precision, balancing false negatives and false positives.
