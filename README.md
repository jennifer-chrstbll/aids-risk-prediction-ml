# AIDS Infection Risk Prediction Using Random Forest and Logistic Regression

## Overview

This project analyzes and compares the performance of Random Forest and Logistic Regression models in predicting AIDS infection risk using clinical and demographic patient data.

The dataset used in this study originates from the AIDS Clinical Trials Group Study 175 dataset from the UCI Machine Learning Repository and was accessed through Kaggle.

The project focuses on addressing common machine learning challenges in medical datasets, including:

- Data imbalance
- Multicollinearity
- Outliers
- Feature normalization

Several preprocessing techniques were implemented to improve model performance and prediction reliability, including:

- Pearson correlation analysis
- Z-score outlier removal
- SMOTE oversampling
- StandardScaler normalization
- Hyperparameter tuning

---

## Features

- AIDS infection risk prediction
- Medical dataset preprocessing
- Random Forest classification
- Logistic Regression classification
- SMOTE imbalance handling
- Correlation heatmap analysis
- Outlier detection and removal
- Hyperparameter tuning
- Model performance comparison

---

## Workflow

![Workflow](images/preprocessing_flow.png)

### Machine Learning Pipeline

```text
Dataset Collection
        ↓
Duplicate & Missing Value Analysis
        ↓
Correlation Analysis
        ↓
Feature Selection
        ↓
Outlier Removal (Z-Score)
        ↓
Train-Test Split
        ↓
SMOTE Oversampling
        ↓
StandardScaler Normalization
        ↓
Model Training
(Random Forest & Logistic Regression)
        ↓
Model Evaluation
```

---

## Dataset

The dataset contains 2,139 patient records with 23 clinical and demographic features.

### Example Features

- Age
- Weight
- Hemophilia history
- Drug usage history
- Karnofsky score
- CD4 count
- CD8 count
- Treatment information

### Target Variable

- `infected`
  - 0 = Not infected
  - 1 = Infected

### Data Source

- UCI Machine Learning Repository
- Kaggle AIDS Virus Infection Prediction Dataset

---

## Technologies Used

### Programming & Analysis

- Python
- Google Colab
- Pandas
- NumPy
- Matplotlib
- Seaborn

### Machine Learning

- Scikit-learn
- Random Forest
- Logistic Regression
- SMOTE
- GridSearchCV
- RandomizedSearchCV

### Preprocessing

- Pearson Correlation
- Z-Score Outlier Detection
- StandardScaler
- Feature Selection

---

## Data Preprocessing

### Duplicate & Missing Value Handling

The dataset was analyzed for duplicate rows and missing values before training.

No missing values or duplicate records were found in the dataset.

### Correlation Analysis

Pearson Correlation analysis was used to identify multicollinearity between features.

Features with very high correlation values (>0.8) were evaluated and removed to improve model stability.

### Outlier Removal

Outliers were removed using the Z-score method with a threshold of ±3.

This preprocessing step reduced the dataset size from:

- 2,139 records
to
- 1,795 records

### SMOTE Oversampling

SMOTE (Synthetic Minority Oversampling Technique) was applied to handle class imbalance between infected and non-infected patients.

### StandardScaler Normalization

Numerical features were normalized using StandardScaler to ensure consistent feature scaling.

---

## Visualizations

### Correlation Heatmap

![Correlation Heatmap](images/correlation_heatmap.png)

### Outlier Visualization (Before)

![Before Outlier Removal](images/age_before_outlier.png)

### Outlier Visualization (After)

![After Outlier Removal](images/age_after_outlier.png)

### SMOTE Distribution

![SMOTE Distribution](images/smote_distribution.png)

---

## Machine Learning Models

### Random Forest

Random Forest achieved the best overall performance with strong accuracy and F1-score results while handling imbalanced medical data effectively.

### Logistic Regression

Logistic Regression also demonstrated good classification performance with lower computational complexity and higher interpretability.

---

## Model Performance

| Model | Accuracy | F1-Score |
|---|---|---|
| Random Forest | 90% | 90% |
| Logistic Regression | 86% | 86% |

Random Forest outperformed Logistic Regression across most evaluation metrics, particularly in detecting the minority infected class.

---

## Evaluation Metrics

The models were evaluated using:

- Accuracy
- Precision
- Recall
- F1-Score

F1-Score was considered especially important due to the imbalanced nature of the medical dataset.

---

## Key Findings

- Random Forest achieved the best predictive performance.
- SMOTE significantly improved minority class detection.
- Proper preprocessing strongly improved model stability.
- Random Forest handled complex feature interactions more effectively than Logistic Regression.
- Logistic Regression remained useful for interpretable and computationally efficient prediction.

---

## Research Paper

[Read Full Paper](paper/paper.pdf)

---

## Google Colab Notebook

[Open in Google Colab](YOUR_COLAB_LINK_HERE)

---

## Repository Structure

```text
aids-risk-prediction-ml/
│
├── README.md
├── LICENSE
├── aids_risk_prediction.ipynb
│
├── paper/
│   └── paper.pdf
│
├── images/
│   ├── preprocessing_flow.png
│   ├── correlation_heatmap.png
│   ├── age_before_outlier.png
│   ├── age_after_outlier.png
│   ├── smote_distribution.png
│   ├── rf_confusion_matrix.png
│   ├── lr_confusion_matrix.png
│   └── model_comparison.png
│
└── data/
    └── sample_dataset.csv
```

---

## Future Improvements

- Implement XGBoost and deep learning approaches
- Expand dataset diversity and size
- Add explainable AI techniques such as SHAP
- Deploy a web-based prediction dashboard
- Compare additional oversampling techniques such as ADASYN

---

## Authors

Machine Learning Research Project  
Universitas Pelita Harapan