# 🚀 NASA Turbofan Jet Engine – RUL Prediction (FD001 Subset)

This project predicts the **Remaining Useful Life (RUL)** of turbofan engines using the **NASA CMAPSS FD001 subset**, applying machine learning models (Random Forest & XGBoost) and visualizing results in **Power BI**.

---

## 📌 Project Goals

- Predict engine failure in advance to enable preventive maintenance.
- Identify which sensors are most useful for forecasting RUL.
- Build a Power BI dashboard to present model insights and sensor trends.

---

## 🧠 Dataset: CMAPSS – FD001 Subset

- Contains time-series sensor data from simulated turbofan engines until failure.
- Each engine unit is monitored over cycles with 21 sensor readings and 3 operational settings.
- Data Source: https://www.kaggle.com/datasets/behrad3d/nasa-cmaps/data

---

## 📊 Workflow Overview

### 1. Data Preprocessing
- Loaded `train_FD001.txt`, removed low-variance sensors.
- Engineered the `RUL` column (based on max cycle per unit).
- Selected top sensors for modeling.

### 2. Modeling (Colab)
- Standardized the data.
- Trained:
  - ✅ Random Forest Regressor
  - ✅ XGBoost Regressor
- Evaluated using **Mean Absolute Error (MAE)**:
  - RF MAE: `~29.64`
  - XGB MAE: `~29.63`

### 3. Feature Importance
- Top sensors for prediction:
  - **Sensor 11** (strong inverse relation to RUL)
  - **Sensor 9**
  - **Sensor 4**

### 4. Power BI Visualization
- Exported a CSV of actual & predicted RUL + key sensors.
- Built Power BI dashboard to visualize:
  - Prediction accuracy (RF vs XGB)
  - Sensor trends vs RUL
  - Sensor Health Index
  

---

## 📈 Power BI Dashboard Highlights

- MAE Gauges for both models
- Actual vs Predicted RUL comparison
- Sensor importance bar charts
- Sensor 11 vs RUL scatter plot (degradation indicator)



---



---

## 🧠 Insights

**Sensor 11**, **Sensor 9**, and **Sensor 4** are most important.
- As **Sensor 11 increases**, **RUL drops** — a strong degradation indicator.
- Models predict RUL with high accuracy.
- Power BI dashboard shows model performance and sensor impact.

---



## 👩‍💻 Author

**Lubna Shaikh**  
`Computer Science | Data Analyst | Python • Power BI • SQL`  


