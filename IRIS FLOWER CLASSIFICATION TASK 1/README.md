# Objective

Train a machine learning model that learns from the measurements of iris flowers and classifies them into one of three species:


  -Iris Setosa
  -Iris Versicolor
  -Iris Virginica

#  Task 1 — Iris Flower Classification

![Python](https://img.shields.io/badge/Python-3.x-blue?style=flat&logo=python)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-ML-orange?style=flat)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=flat)

---

##  Objective

Train a machine learning model that learns from the measurements of iris flowers and classifies them into one of three species:
- *Iris Setosa*
- *Iris Versicolor*
- *Iris Virginica*

---

##  Dataset

| Property       | Value              |
|----------------|--------------------|
| Source         | Kaggle / OIBSIP    |
| Rows           | 150                |
| Features       | 4                  |
| Target Classes | 3                  |
| Missing Values | None               |

**Features:**
- Sepal Length (cm)
- Sepal Width (cm)
- Petal Length (cm)
- Petal Width (cm)

---

##  Exploratory Data Analysis

- Scatter plots across all feature pairs (color-coded by species)
- Box plots showing feature distributions per species
- Key finding: **Petal Length & Petal Width** are the most separating features for classification

---

## 🤖 Models Trained

| Model               | Accuracy |
|---------------------|----------|
| Logistic Regression | 96.67% 🏆|
| SVM (RBF Kernel)    | 96.67%   |
| Decision Tree       | 93.33%   |
| Random Forest       | 90.00%   |

---

##  Best Model — Logistic Regression

- **Accuracy:** 96.67%
- **Setosa:** 100% precision & recall
- **Versicolor:** 100% precision, 90% recall
- **Virginica:** 91% precision, 100% recall
- **Overall F1-Score:** 0.97

---

##  Files

| File | Description |
|------|-------------|
| `iris_classification.py` | Full ML pipeline script |
| `Iris.csv` | Dataset |
| `README.md` | This file |

---

##  How to Run

```python
# 1. Open Google Colab
# 2. Upload Iris.csv
# 3. Paste iris_classification.py into a cell
# 4. Run — plots will appear inline
```

---

## 📈 Results

- Confusion matrix shows near-perfect classification
- Setosa is perfectly linearly separable from the other two species
- Versicolor and Virginica have slight overlap which causes the 1 misclassification
