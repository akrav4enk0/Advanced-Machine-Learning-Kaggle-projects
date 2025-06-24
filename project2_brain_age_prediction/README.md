# 🧠 Brain Age Prediction from MRI Features  
*ETH Zurich – Advanced Machine Learning Course Project*

**Public Leaderboard R² Score**: ~0.76 (top 9 position out of 287 Participants / 150 Teams) 

---

## 📘 Overview

This repository contains my project to the **Brain Age Prediction** task from the **Advanced Machine Learning course** at ETH Zurich. The goal is to predict biological brain age using noisy, high-dimensional MRI features. This project emphasizes realistic challenges in medical data science, including missing data, feature selection, and overfitting prevention.

> ✨ This is a complete, educational walkthrough designed for students and practitioners interested in reproducible machine learning workflows.

---

## 📂 Structure

| Path                    | Description                                           |
|-------------------------|-------------------------------------------------------|
| `notebook/`             | Jupyter notebook with full pipeline implementation   |
| `results/`              | Final submission files                               |
| `figures/` (to be added)| Visualizations (R² plots, prediction snapshots, etc.)|
| `requirements.txt`      | Python dependencies                                  |
| `README.md`             | This file                                            |

---

## 📊 Dataset Description

> *Dataset files are not included due to competition restrictions.*

- `X_train.csv`: 831 features, 1212 samples (training)
- `y_train.csv`: brain age in years
- `X_test.csv`: 831 features, 776 samples (test, no labels)
- `sample.csv`: submission format template

---

## 🔍 Methodology

### 1. Data Preprocessing

- **Missing Values**:  
  Compared missing rates in training/test sets. Applied `SimpleImputer` (median) and `KNNImputer` (k=20) based on performance.

- **Outlier Removal**:  
  Used `ECOD` from the `pyod` library to remove ~1% most anomalous samples.

- **Feature Engineering**:  
  - Dropped constant features  
  - Dropped highly correlated features  
  - Applied `SelectKBest(f_regression)` for relevance scoring  
  - Removed features with high missing ratios  
  - Final feature set: ~250 features

- **Scaling**:  
  `StandardScaler` used for all models

### 2. Model Training

GridSearchCV used to tune models individually:

| Model                  | Best CV R² Score |
|------------------------|------------------|
| SVR (RBF/RQ kernels)   | ~0.61            |
| CatBoostRegressor      | ~0.58            |
| Cubist (sklego)        | ~0.57            |
| GradientBoosting       | ~0.57            |
| ExtraTreesRegressor    | ~0.55            |

### 3. Stacking Ensemble

- Base Models: SVR, CatBoost, Cubist, ExtraTrees, GBR  
- Meta-model: RidgeCV  
- Final performance: **~0.76 R² on public leaderboard**

---

## 💡 Educational Features

✅ Inline code explanations  
✅ Custom preprocessing transformers  
✅ Clear feature selection rationale  
✅ Visual diagnostics for model performance  
✅ Clean pipeline modularization

---

## 📚 How to Run

1. Clone the repo:
```bash
git clone https://github.com/your-username/brain-age-prediction.git
cd brain-age-prediction
```

2. Create a virtual environment and install dependencies:
```bash
pip install -r requirements.txt
```

3. Launch Jupyter:
```bash
jupyter notebook notebook/brain_age_prediction.ipynb
```

---

## About

Anna Kravchenko  
Master’s Student @ ETH Zurich (Data Science)  
| Passionate about open science and reproducibility  

---

## License

This project is shared under the MIT License.
