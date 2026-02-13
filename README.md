# 🚗 Vehicle Sales Price Prediction & Market Analysis

## 📊 Overview

This project delivers an end-to-end machine learning pipeline for predicting vehicle selling prices using historical sales data. It integrates advanced data preprocessing, exploratory analytics, statistical testing, and ensemble regression modeling to uncover pricing drivers and generate high-accuracy predictions.

The workflow demonstrates the complete data science lifecycle — from raw data ingestion to predictive modeling and evaluation.

---

## 🎯 Objectives

- Clean and preprocess vehicle sales data containing missing values and outliers  
- Perform exploratory data analysis to uncover trends and pricing patterns  
- Train and evaluate machine learning models for price prediction  
- Identify key factors influencing vehicle resale value  

---

## 📋 Dataset Description

Historical vehicle transaction records with structured attributes:

### Vehicle Information
- **Year** — Manufacturing year  
- **Make** — Brand name  
- **Model** — Vehicle model  
- **Trim** — Variant/version  
- **Body** — SUV, Sedan, etc.  

### Technical & Condition
- **Transmission** — Automatic / Manual  
- **Condition** — Sale condition rating  
- **Odometer** — Mileage  

### Visual & Identification
- **Color** — Exterior  
- **Interior** — Cabin material/color  
- **VIN** — Unique identifier  

### Market & Transaction
- **State** — Sale location  
- **Seller** — Seller type  
- **MMR** — Market benchmark price  
- **Selling Price** — Target variable  
- **Sale Date** — Transaction date  

---

## 🛠️ Tech Stack

- **Python**
- **Pandas, NumPy**
- **Matplotlib, Seaborn**
- **Scikit-learn**
- **XGBoost**
- **CuML (GPU Random Forest)**

---

## 🧹 Data Preprocessing

Key preparation steps:

- Column normalization and renaming  
- State code → full name mapping  
- Brand clustering and standardization  
- Intelligent missing value imputation  
  - Vehicle attributes → similarity mapping  
  - Prices → grouped mean estimation  
  - Colors/interiors → mode filling  
- VIN-based duplicate removal  
- Outlier detection:
  - IQR filtering  
  - Isolation Forest anomaly detection  

---

## 📈 Exploratory Data Analysis

- Descriptive statistical summaries  
- Brand-wise sales distribution  
- Price spread and boxplot analysis  
- MMR vs Selling Price correlation  
- State-level sales concentration  

---

## 🧪 Statistical Testing

**Transmission Pricing Impact**
- T-test: Automatic vs Manual price comparison  

**Mileage Effect**
- Z-test: High vs Low odometer price impact  

---

## 🤖 Machine Learning Models

### Polynomial Regression (Degree 2)
- Captures nonlinear relationships  
- **R²: 0.95**

### XGBoost Regressor
- Gradient boosting ensemble  
- Strong predictive performance  
- **R²: 0.95**

### Random Forest Regressor
- Bagging ensemble model  
- GridSearchCV optimized  
- GPU accelerated (CuML)  
- **R²: 0.93 → 0.95**

---

## ⚙️ Modeling Pipeline

- One-hot encoding (categorical features)  
- Standard scaling (numerical features)  
- Train/Test split — 80/20  
- Hyperparameter tuning  
- Cross-validation  

---

## 📊 Model Performance

| Model | R² Score | MAE | MSE |
|------|-----------|------|------|
| Polynomial Regression | 0.95 | ~1019 | ~2,268,165 |
| XGBoost | 0.95 | — | — |
| Random Forest | 0.93–0.95 | — | — |

---

## 🔍 Key Insights

- **MMR vs Selling Price correlation ≈ 0.97**  
- Luxury brands show higher median price variance  
- Ford, Chevrolet, Nissan dominate sales volume  
- California & Texas lead sales distribution  
- Transmission type significantly impacts price  

---

## 📁 Project Structure

```
Vehicle_sales/
├── Vehicle_Sales_Final.ipynb    # Main Jupyter notebook
├── README.md                     # Project documentation
└── index.html                    # HTML export of the notebook
```

---

## 🚀 Run Instructions

### 1️⃣ Clone Repository

```bash
git clone https://github.com/yourusername/Vehicle_sales.git
cd Vehicle_sales
```
### 2️⃣ Create Virtual Environment
```bash
venv\Scripts\activate
```
### 3️⃣ Install Dependencies
```bash
pip install -r requirements.txt
```
### Open:
```
Vehicle_Sales_Final.ipynb

```
## 🧠 Methodology
Data ingestion

Cleaning & deduplication

Feature transformation

Outlier detection

Exploratory analysis

Feature engineering

Model training

Hyperparameter tuning

Evaluation & visualization


## 🔮 Future Enhancements

Deep neural regression models

Time-series depreciation modeling

Web app deployment (Flask / Streamlit)

Advanced feature engineering

Stacked ensemble learning
