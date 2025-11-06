# 🌫️ Air Quality Index (AQI) Prediction Model

This project was developed as part of my **AICTE Virtual Internship in AI & Data Analytics**, organized by **Shell India Pvt. Ltd.** and **Edunet Foundation**.  
The goal of this project is to **predict the Air Quality Index (AQI)** of various Indian cities based on air pollutant concentration levels using **Machine Learning regression models**.

---

## 📂 Project Overview

Air pollution is a major environmental issue in urban areas.  
The **AQI (Air Quality Index)** is a numerical scale used to describe the quality of air and the level of health concern associated with it.

In this project:
- Historical air quality data was collected and analyzed.
- Missing values and outliers were treated.
- The dataset was preprocessed, scaled, and modeled using multiple regression algorithms.
- The best-performing model was selected based on performance metrics like **R² score** and **Root Mean Square Error (RMSE)**.

---

## 🧠 Key Features

- Data preprocessing, cleaning, and imputation of missing values.
- Outlier detection and handling using the IQR (Interquartile Range) method.
- Feature scaling using **StandardScaler**.
- Visualization of pollutants and AQI distribution using **Matplotlib** and **Seaborn**.
- Machine Learning models implemented:
  - Linear Regression
  - K-Nearest Neighbors (KNN)
  - Decision Tree Regressor
  - Random Forest Regressor
- Performance evaluation using RMSE and R² metrics.

---

## 🗃️ Dataset

The dataset used is `air quality data.csv`, which contains city-wise daily air pollution measurements from 2015–2020.

**Columns include:**
- PM2.5, PM10, NO, NO₂, NOx, NH₃, CO, SO₂, O₃, Benzene, Toluene, Xylene
- AQI and AQI_Bucket
- City, Date

**Shape:** 29,531 rows × 16 columns  
**Source:** Public dataset provided in AICTE internship program.

---

## ⚙️ Workflow Summary

### **1. Data Cleaning & Preprocessing**
- Removed duplicate entries and irrelevant columns.
- Dropped rows with missing `AQI` values.
- Replaced remaining NaN values with mean pollutant values.
- Removed outliers using the IQR method.

### **2. Data Visualization**
- Plotted histograms for pollutant distributions.
- Created box plots and city-wise pollutant comparisons.
- Correlation heatmap to identify strong predictors of AQI.

### **3. Model Building**
- Target variable: `AQI`
- Features: All other pollutant columns.
- Data split: 80% Training, 20% Testing
- Scaling applied using `StandardScaler`.

### **4. Model Evaluation**
| Model | RMSE (Test) | R² Score (Test) |
|--------|--------------|----------------|
| Linear Regression | 0.58 | 0.65 |
| KNN Regressor | 0.47 | 0.77 |
| Decision Tree Regressor | 0.55 | 0.68 |
| **Random Forest Regressor** | **0.38** | **0.84** |

✅ **Best Model:** Random Forest Regressor

---

## 🧾 Libraries Used

```python
pandas
numpy
matplotlib
seaborn
scikit-learn
