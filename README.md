# Advanced Machine Learning - Kaggle Competition Projects for ETH Zurich  

This repository contains three machine learning projects completed as part of the **Advanced Machine Learning (AML)** course at **ETH Zurich**. Each project addresses a different classification or regression problem derived from a Kaggle-style competition, with the goal of developing and optimizing predictive models using various preprocessing, feature selection, and ensemble strategies.

---

## 🔬 Projects Overview

### 📁 Project1_Iris_Classification
**Task:** Multiclass classification of iris flower species (Setosa, Versicolor, Virginica)  
**Techniques:**
- Preprocessing with missing value handling, feature scaling
- Dimensionality reduction with PCA
- Training multiple classifiers: Logistic Regression, KNN, Decision Tree, Random Forest
- Model performance evaluation and visualization
- Final submission using the best-performing model based on cross-validation accuracy

👉 [View README](Project1_Iris_Classification/README.md)
👉 [View notebook](Project1_Iris_Classification/iris_classification.ipynb)

---

### 📁 Project2_Brain_Age_Prediction
**Task:** Regression problem to predict brain age based on extracted features from brain MRI scans  
**Techniques:**
- Data cleaning, outlier removal, and correlation filtering
- Feature selection with SelectKBest and model-based ranking
- Model training using: Ridge Regression, Random Forest, Gradient Boosting Regressor
- Stacking ensemble of top models
- Best score achieved with a tuned Gradient Boosting Regressor model

👉 [View README](project2_brain_age_prediction/README.md)
👉 [View notebook](project2_brain_age_prediction/notebook.ipynb)

---

### 📁 project3_Heart_Rhythm_Classification
**Task:** Classification of ECG signals into different heart rhythm classes  
**Techniques:**
- Custom feature engineering from raw ECG time series (mean, std, skew, kurtosis, pNN, wavelet transforms, etc.)
- Feature selection and removal of correlated features
- Outlier detection
- Model benchmarking: SVC, MLP, Random Forest, GBC, Logistic Regression
- Final model: Gradient Boosting Classifier fine-tuned with a custom function, achieving the best private leaderboard score on test data

👉 [View README](project3_heart_rhythm_classification/README.md)
👉 [View notebook](project3_heart_rhythm_classification/ecg_classifier.ipynb)

---

## 📦 Folder Structure

```bash
Advanced-Machine-Learning-Kaggle-projects/
├── Project1_Iris_Classification/
├── project2_brain_age_prediction/
├── project3_heart_rhythm_classification/
└── README.md
