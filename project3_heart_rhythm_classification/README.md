# 🫀 ECG Heart Rhythm Classification

This project addresses the task of classifying ECG signals into distinct heart rhythm classes using a comprehensive and reproducible machine learning pipeline. The work was conducted independently as part of the **Advanced Machine Learning** course at **ETH Zurich**, and submitted within a Kaggle competition.

> 📘 This is a complete, educational walkthrough designed for students and practitioners interested in reproducible machine learning workflows.

---

## Problem Statement

The objective of this project was to develop an accurate classification model for ECG time-series data, with the aim of identifying the correct heart rhythm class for each input sample. Each sample consisted of a one-dimensional ECG signal captured over a fixed time period.

---

## Approach

A classical machine learning workflow was adopted with a strong emphasis on robust feature engineering and thorough model evaluation.

### 1. 🔍 Feature Extraction

An extensive set of descriptive statistical and signal-processing-based features was engineered from the raw ECG signals, including:

- **Basic statistics**: mean, standard deviation, skewness, kurtosis, and quantiles
- **Temporal and inter-peak features**: differences, ratios, pNN metrics, log-RSMMD
- **Signal-to-noise ratios**
- **Frequency domain features**: wavelet-based signal transformations via Fourier analysis

These features were computed on raw ECG data and, when appropriate, on signal segments surrounding detected QRS peaks to better capture physiologically relevant characteristics.

### 2. ⚙️ Preprocessing Pipeline

To ensure the models performed effectively and reliably, the following preprocessing steps were applied:

- **Standardization** of all features to enforce uniform scale
- **Correlation filtering** to remove highly collinear features
- **Univariate feature selection** using `SelectKBest` with mutual information
- **Outlier detection and removal** using IQR and z-score-based techniques

These steps helped improve generalization, reduce overfitting, and enhance training efficiency.

### 3. Model Development

Multiple classification algorithms from the `scikit-learn` ecosystem were explored, including:

- Logistic Regression
- Support Vector Classification (SVC)
- Random Forest
- Gradient Boosting Classifier (GBC)
- Multi-Layer Perceptron (MLP)
- AdaBoost
- Gaussian Process
- VotingClassifier ensembles

Each model underwent rigorous hyperparameter tuning using `GridSearchCV` to maximize validation performance.

---

## 🏆 Best Model and Submissions

The final and best-performing model was a **Gradient Boosting Classifier**, selected based on validation score performance. A custom optimization loop was implemented to refine both the feature selection and hyperparameter space simultaneously.

### ✅ Submission Highlights

| Submission | Model                                      | Validation Score |
|------------|---------------------------------------------|------------------|
| #9         | Gradient Boosting Classifier (custom tuned) | **0.83178**      |
| #10        | Ensemble (Random Forest + GBC)              | 0.82482          |
| #6         | Ensemble (SVC + RF + GBC + ExtraTrees)      | 0.82540          |

The final submission (#9) stood out for its balance of accuracy, interpretability, and robustness.

---

## 📂 Repository Structure

```bash
project3_heart_rhythm_classification/
├── ecg_classifier.ipynb         # Full pipeline: preprocessing, training, and evaluation
├── submission_*.csv             # Prediction files for competition submission
├── feature_engineering.py       # Modularized feature extraction functions
├── model_utils.py               # Hyperparameter search and model training helpers
└── README.md                    # Project documentation

