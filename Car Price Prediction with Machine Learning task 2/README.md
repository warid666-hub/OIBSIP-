# 🚗 Task 2 — Car Price Prediction

![Python](https://img.shields.io/badge/Python-3.x-blue?style=flat&logo=python)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-ML-orange?style=flat)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=flat)

---

##  Objective

Build a machine learning model that predicts the **selling price of a used car** based on features like present price, fuel type, transmission, kilometers driven, and age of the car.

---

##  Dataset

| Property       | Value           |
|----------------|-----------------|
| Rows           | 301             |
| Features       | 8               |
| Target         | Selling Price   |
| Missing Values | None            |

**Features:**
- Car Name
- Year → converted to **Car Age**
- Present Price
- Driven KMs
- Fuel Type (Petrol / Diesel / CNG)
- Selling Type (Dealer / Individual)
- Transmission (Manual / Automatic)
- Owner

---

##  Feature Engineering

- Created `Car_Age = 2025 - Year` (more meaningful than raw year)
- Dropped `Car_Name` and `Year`
- Label encoded categorical columns: `Fuel_Type`, `Selling_type`, `Transmission`

---

##  Exploratory Data Analysis

- Selling price distribution histogram
- Present Price vs Selling Price scatter plot
- Car Age vs Selling Price scatter plot
- Fuel Type & Transmission box plots
- Correlation heatmap
- Key finding: **Present Price** and **Car Age** are the strongest predictors

---

##  Models Trained

| Model               | R² Score | MAE    | RMSE   |
|---------------------|----------|--------|--------|
| Linear Regression   | ~0.87    | ~1.22  | ~1.98  |
| Decision Tree       | ~0.93    | ~0.85  | ~1.42  |
| **Random Forest**   | **~0.96**| ~0.71  | ~1.08  |
| Gradient Boosting   | ~0.95    | ~0.76  | ~1.18  |

---

##  Best Model — Random Forest

- **R² Score:** ~0.96 (explains 96% of price variance)
- Lowest MAE and RMSE among all models
- Most important features: **Present Price**, **Car Age**, **Driven KMs**

---

##  Files

| File | Description |
|------|-------------|
| `car_price_prediction.py` | Full ML pipeline script |
| `car_data.csv` | Dataset |
| `README.md` | This file |

---

##  How to Run

```python
# 1. Open Google Colab
# 2. Run the script — it will prompt you to upload car_data.csv
# 3. All EDA and result plots appear inline
```

---

##  Results

- Random Forest achieved the best R² of ~0.96
- Present Price is the single most important feature
- Car Age has a strong negative correlation with selling price
- Automatic transmission cars tend to have higher selling prices
