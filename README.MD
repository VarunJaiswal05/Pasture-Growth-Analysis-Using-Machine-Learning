# Pasture Growth Prediction — Large-Scale ML

> Predicting Total Seasonal Dry Matter (pasture growth) across Queensland from 33 million+ environmental records, comparing Random Forest against XGBoost.

![Python](https://img.shields.io/badge/Python-3-3776AB?style=flat-square&logo=python&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-Random%20Forest-F7931E?style=flat-square&logo=scikit-learn&logoColor=white)
![XGBoost](https://img.shields.io/badge/XGBoost-Regressor-EB0000?style=flat-square)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Wrangling-150458?style=flat-square&logo=pandas&logoColor=white)

QUT Advanced Capstone (IFN703), June to November 2024.

---

## 📌 Overview

Pasture growth (Total Seasonal Dry Matter, TSDM) drives grazing capacity and stocking decisions for Queensland agriculture, but it's expensive to measure directly at scale. This project builds and compares two regression models that predict TSDM from climate and satellite data alone, and identifies which environmental factors actually move the needle.

## 📊 Dataset

- 33 million+ records combining SILO climate data and satellite-derived pasture measurements across Queensland
- Features: rainfall, max/min temperature, humidity, evaporation, solar radiation, paddock land size, year and month
- Engineered features: temperature range, month-based historical averages for temporal smoothing

## 🔍 Methodology

- `SelectKBest` feature selection to narrow the environmental variables down to the most predictive set (Year, EVAP, RADIATION, Temp_Range, RH_TMAX, MIN_TEMP, MAX_TEMP)
- 80/20 train/test split
- Two models trained and compared: **Random Forest Regressor** and **XGBoost Regressor**
- `RandomizedSearchCV` hyperparameter tuning on both
- Multi-metric evaluation: R², RMSE, MAE, not just one headline number

## 📈 Results

![Correlation matrix of climate and TSDM variables](pasture-correlation-matrix.png)

Random Forest was the stronger model, R² ≈ 0.717 against XGBoost's R² ≈ 0.664.

![Feature importance from the Random Forest model](pasture-feature-importance.png)

Year was by far the dominant predictor, well ahead of evaporation and solar radiation, which suggests a meaningful year-on-year trend in the data beyond seasonal weather alone.

![Actual vs predicted values](pasture-actual-vs-predicted.png)

![Historical vs predicted monthly mean TSDM](pasture-predicted.png)

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| Python | Core language |
| Pandas / NumPy | Data merging, cleaning, feature engineering |
| scikit-learn | Random Forest, `SelectKBest`, `RandomizedSearchCV` |
| XGBoost | Gradient-boosted regression model |
| Matplotlib / Seaborn | All result visualisations |

## 📁 Files

- [`PG-UP-1.ipynb`](PG-UP-1.ipynb) — full analysis notebook
- [`IFN703_Varun_Vikas_Jaiswal_n11736089.pdf`](IFN703_Varun_Vikas_Jaiswal_n11736089.pdf) — exported report

---

**Author:** Varun Vikas Jaiswal (QUT, 2024)
