#  Task 4 — Email Spam Detector

![Python](https://img.shields.io/badge/Python-3.x-blue?style=flat&logo=python)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-ML-orange?style=flat)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=flat)

---

##  Objective

Build a machine learning model that classifies email/SMS messages as **Spam** or **Ham (not spam)** using natural language processing and text classification techniques.

---

##  Dataset

| Property       | Value             |
|----------------|-------------------|
| Rows           | 5,572             |
| Classes        | Ham, Spam         |
| Ham            | 4,825 (86.6%)     |
| Spam           | 747 (13.4%)       |
| Missing Values | None              |

Dataset is imbalanced, which is typical and expected for real-world spam detection.

---

##  Text Preprocessing

- Converted text to lowercase
- Removed URLs
- Removed numbers
- Removed punctuation
- Stripped extra whitespace
- Vectorized using **TF-IDF** (max 3,000 features, English stop words removed)

---

##  Exploratory Data Analysis

- Ham vs Spam class distribution (pie chart)
- Message length distribution by class
- Word count comparison (box plot)
- Top frequent words found in spam messages

**Key finding:** Spam messages tend to be longer and contain words like "free", "win", "claim", "urgent", and "txt".

---

##  Models Trained

| Model               | Accuracy | F1-Score |
|----------------------|----------|----------|
| Naive Bayes          | 97.04%   | 0.876    |
| Logistic Regression  | 96.41%   | 0.846    |
| **SVM (Linear)**     | **98.39%** 🏆 | **0.937** |
| Random Forest        | 97.58%   | 0.900    |

F1-score (not just accuracy) is used to select the best model since the dataset is imbalanced.

---

##  Best Model — SVM (Linear Kernel)

- **Accuracy:** 98.39%
- **F1-Score:** 0.937
- Performs best at separating spam from ham with minimal false positives

---

##  Files

| File | Description |
|------|-------------|
| `spam_detector.py` | Full ML pipeline script |
| `spam.csv` | Dataset |
| `README.md` | This file |

---

##  How to Run

```python
# 1. Open Google Colab
# 2. Run the script — it will prompt you to upload spam.csv
# 3. All EDA and result plots appear inline
```

---

##  Results

- TF-IDF vectorization combined with SVM gave the best results
- Model correctly classifies real spam patterns (won, free, urgent, click here)
- Tested successfully on unseen custom messages at the end of the script

---

##  Sample Predictions

| Message | Prediction |
|---------|------------|
| "Congratulations! You've won a free iPhone..." | SPAM |
| "Hey, are we still on for lunch tomorrow?" | HAM |
| "URGENT: Your account will be suspended..." | SPAM |
| "Can you send me the report by end of day?" | HAM |
