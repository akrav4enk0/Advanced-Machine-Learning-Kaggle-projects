# 🌸 Iris Flower Classification

**ETH Zurich – Advanced Machine Learning Course Project**

This repository contains a complete machine learning pipeline for classifying **Iris flower species** based on flower measurements. The goal is to provide an educational, easy-to-follow notebook demonstrating the core steps of a classification task.

> 📘 This project is structured as an educational guide. Every section of the pipeline is clearly described and easy to reproduce or adapt for new learners in data science and machine learning.

---

## 📁 Repository Structure

| File / Folder          | Description                                      |
|------------------------|--------------------------------------------------|
| `notebooks/`           | Jupyter notebook with detailed ML pipeline       |
| `data/`                | `train.csv` and `test.csv` files (user-provided) |
| `submission_*.csv`     | Example submission files from different models   |
| `README.md`            | You are here! Project overview and instructions  |

---

## 📦 Dataset

The dataset includes numeric features for flower dimensions and a label indicating the **species**.

- `train.csv`: labeled data for training the model
- `test.csv`: test data without labels
- `sample_submission.csv`: sample format for predictions

---

## 🔍 Project Workflow

### 1. 📊 Data Preprocessing
- Checked and confirmed no missing values in train and test sets
- Ensured consistent feature format
- Encoded labels using `LabelEncoder` for classification

### 2. 📈 Exploratory Data Analysis
- Visualized class distribution
- Reviewed pairplots and feature relationships
- Verified class balance

### 3. ⚙️ Model Training
Trained several classification models and evaluated their performance:

| Model               | Description                            |
|--------------------|----------------------------------------|
| Logistic Regression| Baseline model                         |
| Decision Tree      | Simple tree-based classifier            |
| Random Forest      | High-performing ensemble model          |
| Naive Bayes        | Probabilistic classifier (used in final submission) |

Final model predictions were exported for submission using:

```python
submission_df_nb.to_csv('submission_7.csv', index=False)

---

 🎓 Educational Goals
This repository was created to:

- Help beginners learn how to handle classification tasks
- Illustrate a clean end-to-end ML workflow
- Compare different classification algorithms
- Provide reusable code for similar problems

---

💻 Getting Started

Clone the repository:

git clone https://github.com/your-username/iris-flower-classification.git
cd iris-flower-classification
(Optional) Create and activate a virtual environment

Install dependencies (basic packages used: pandas, sklearn, numpy, matplotlib, seaborn)

Launch the notebook:
jupyter notebook notebooks/iris_classification.ipynb


✍️ Author
Anna Kravchenko
Master’s Student @ ETH Zurich
💡 Interested in making machine learning education accessible and reproducible.

📄 License
MIT License — free to use, modify, and distribute with attribution.
