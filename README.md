# 🏥 AI-Based Hospital Bed Availability Prediction System

## 📌 Project Overview
This project focuses on predicting next-day hospital bed occupancy using machine learning. It uses historical hospital data such as admissions, discharges, ICU usage, and operational metrics to forecast future bed demand.

---

## 🎯 Objective
- Prepare a forecasting-ready dataset
- Apply time-series feature engineering
- Build a baseline prediction model
- Support hospital resource planning

---

## 📊 Dataset Features
- date
- hospital_branch
- weekday
- total_beds
- icu_beds
- occupied_beds
- occupied_icu_beds
- available_beds
- admissions
- discharges
- emergency_cases
- staff_available

---

## ⚙️ Data Preprocessing
- Removed duplicate records
- Verified no missing values
- Converted date column to datetime format
- Sorted data chronologically

---

## 🧠 Feature Engineering
- Lag Features (lag_1, lag_2)
- Rolling Mean (3-day average)
- Occupancy Rate
- ICU Utilization
- One-hot encoding for categorical variables

---

## 🎯 Target Variable
Target created using next-day occupancy:

target = occupied_beds.shift(-1)

---

## 📈 Exploratory Data Analysis (EDA)
- Time-series occupancy trend visualization
- Correlation heatmap analysis
- Strong dependency observed on lag features

---

## 🤖 Model Used
- Linear Regression (Baseline Model)
- Time-based train-test split (no shuffle)

---

## 📊 Model Performance
- MAE: ~35.55
- R² Score: ~ -0.069

### 📌 Interpretation
- Model performance is weak
- Indicates non-linear and complex patterns in data
- Serves as a baseline for future improvements

---

## 🚀 Future Improvements
- Random Forest Regressor
- XGBoost
- LSTM (Deep Learning)
- Real-time dashboard using Streamlit

---

## 📁 Project Structure
AI_Hospital_Bed_Prediction_Project/
│
├── data/
├── notebooks/
├── outputs/
├── README.md

---

## 🧑‍💻 Author
Sourav Kumar

---

## 📌 Conclusion
This project builds an end-to-end machine learning pipeline for hospital bed occupancy prediction. It highlights the importance of time-series feature engineering and provides a strong foundation for advanced predictive models.