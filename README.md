# 🛒 Retail Demand Forecasting using Machine Learning

> A machine learning project for forecasting weekly retail demand across multiple supermarkets using historical sales and promotional data.

![Python](https://img.shields.io/badge/Python-3.11-blue)
![LightGBM](https://img.shields.io/badge/LightGBM-Model-success)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-ML-orange)
![License](https://img.shields.io/badge/License-MIT-green)

---

# 📌 Project Overview

Accurate demand forecasting is essential for effective inventory management in retail businesses. Poor demand estimation can lead to:

- 📉 Stock-outs (lost sales)
- 📦 Excess inventory
- 💰 Increased storage costs
- 📊 Inefficient supply chain planning

This project develops a machine learning-based forecasting pipeline to predict **weekly product demand** for different supermarket-SKU combinations **8 weeks in advance**.

The complete workflow includes:

- Data Cleaning
- Exploratory Data Analysis (EDA)
- Feature Engineering
- Walk-Forward Time-Series Validation
- LightGBM Forecasting Model
- Business Performance Evaluation

---

# 🎯 Problem Statement

The objective is to forecast weekly demand for every supermarket and product (SKU) combination using historical demand and promotional information.

The model is designed to:

- Forecast demand 8 weeks ahead
- Capture seasonality and demand trends
- Measure promotion impact
- Support inventory planning decisions

---

# 📂 Repository Structure

```
Retail-Demand-Forecasting/

│── Demand_Forecasting.ipynb
│── README.md
│── requirements.txt

├── data/
│   ├── demand.csv
│   └── promotions.csv

├── outputs/
│   ├── prediction_results.csv
│   ├── feature_importance.png
│   └── forecast_example.png

└── models/
    └── final_model.pkl
```

---

# 📊 Dataset

The project uses two datasets.

### demand.csv

Contains historical weekly demand information.

Features include:

- Date
- Supermarket
- SKU
- Weekly Demand

---

### promotions.csv

Contains promotional campaign information.

Features include:

- Promotion Start Date
- Promotion Duration
- Supermarket
- SKU

---

# ⚙️ Project Workflow

## 1️⃣ Data Cleaning

- Missing value treatment
- Duplicate checking
- Outlier detection
- Data consistency verification

---

## 2️⃣ Exploratory Data Analysis

Performed detailed analysis to understand:

- Demand distribution
- Weekly trends
- Seasonality
- Promotion impact
- SKU-wise demand
- Supermarket-wise demand

---

## 3️⃣ Feature Engineering

Created forecasting features including:

- Lag Features
- Rolling Statistics
- Promotion Indicators
- Calendar Features
- Historical Demand Patterns

---

## 4️⃣ Model Development

The forecasting model was built using **LightGBM Regressor**.

Reasons for selecting LightGBM:

- Fast training
- Handles non-linear relationships
- Works well on tabular datasets
- Robust for forecasting problems

---

## 5️⃣ Time-Series Validation

Instead of using a random train-test split, this project implements **Walk-Forward Validation**, which better represents real-world forecasting scenarios.

Benefits include:

- No future information leakage
- Realistic evaluation
- Better estimation of production performance

---

## 📈 Model Evaluation

The model was evaluated using multiple forecasting metrics.

| Metric | Value |
|---------|--------|
| MAE | 11.99 |
| RMSE | 18.49 |
| R² Score | 0.9787 |
| MAPE | 2.21% |
| WAPE | 2.27% |

A simple **Naive Forecast** was also implemented as a baseline for comparison.

---

# 📉 Feature Importance

The model identifies the most influential variables affecting demand.

Key features include:

- Historical Demand
- Promotion Activity
- Calendar Features
- Lag Variables
- Rolling Statistics

Feature importance visualization is included in the notebook.

---

# 💼 Business Insights

The analysis provides several practical insights:

- Promotional campaigns increase product demand.
- Historical demand is the strongest predictor.
- Weekly seasonality significantly affects sales.
- Demand patterns vary across supermarkets and products.

These insights can help businesses improve:

- Inventory Planning
- Stock Replenishment
- Warehouse Management
- Promotion Strategy

---

# 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-Learn
- LightGBM
- Joblib

---

# 🚀 How to Run

### Clone Repository

```bash
git clone https://github.com/Raghav1507/Retail-Demand-Forecasting.git
```

---

### Install Dependencies

```bash
pip install -r requirements.txt
```

---

### Launch Jupyter Notebook

```bash
jupyter notebook
```

Open:

```
Demand_Forecasting.ipynb
```

---

# 📌 Future Improvements

Potential enhancements include:

- Hyperparameter Optimization
- Holiday and Festival Features
- Weather Data Integration
- Ensemble Models
- Deep Learning (LSTM/Transformer)
- Automated Forecast Dashboard

---

# 👨‍💻 Author

**Raghav Singhal**

B.Tech CSE (Artificial Intelligence & Machine Learning)

Interested in:

- Machine Learning
- Data Science
- Time-Series Forecasting
- Predictive Analytics

GitHub:
https://github.com/Raghav1507

---

# ⭐ Acknowledgements

This project was developed as part of a demand forecasting case study to demonstrate practical machine learning techniques for retail inventory management.
