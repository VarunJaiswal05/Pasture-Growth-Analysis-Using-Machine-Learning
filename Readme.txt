Pasture Growth Analysis Using Machine Learning
==============================================

This project was developed for IFN703 - Advanced Data Analytics 
at Queensland University of Technology (QUT).

It focuses on predicting Total Seasonal Dry Matter (TSDM) for pasture 
growth using two supervised machine learning techniques:
Random Forest Regressor and XGBoost Regressor.


--------------------------------------------------------------
OBJECTIVE
--------------------------------------------------------------
To develop a predictive model that estimates pasture productivity 
(Total Seasonal Dry Matter - TSDM) based on environmental and 
temporal variables.

The project aims to:
- Identify the key environmental factors affecting pasture growth
- Compare ensemble-based regression models for accuracy
- Enable short-term forecasting using historical feature averages


--------------------------------------------------------------
DATASETS USED
--------------------------------------------------------------
The dataset combines field-based pasture measurements and 
meteorological variables including:

- Rainfall (RAIN)
- Maximum Temperature (MAX_TEMP)
- Minimum Temperature (MIN_TEMP)
- Relative Humidity (RH_TMAX, RH_TMIN)
- Evaporation (EVAP)
- Solar Radiation (RADIATION)
- Crop Type, Land Size, Paddock ID, and Observation Date

Region: Queensland, Australia
Time Period: Multiple seasonal observations (aggregated monthly)


--------------------------------------------------------------
FEATURES ENGINEERED
--------------------------------------------------------------
- Temp_Range = MAX_TEMP - MIN_TEMP
- Month-based historical averages for feature smoothing
- Encoded temporal variables (Month, Year)
- Standardization and scaling of numeric features
- Removal of outliers and handling of missing data


--------------------------------------------------------------
MODELS USED
--------------------------------------------------------------
1. Random Forest Regressor
   - Captures nonlinear feature interactions
   - Provides feature importance scores
   - High interpretability and stability

2. XGBoost Regressor
   - Gradient boosting framework with regularization
   - Optimized for performance and generalization


--------------------------------------------------------------
RESULTS & INSIGHTS
--------------------------------------------------------------
- Random Forest achieved R² ≈ 0.717 on the test set
- XGBoost achieved R² ≈ 0.664 on the test set
- Top predictive variables:
  • Year
  • Evaporation
  • Radiation
- The month-based historical feature averages improved 
  short-term prediction reliability
- Both models effectively captured seasonal variability in pasture growth


--------------------------------------------------------------
CONCLUSIONS
--------------------------------------------------------------
The study demonstrates that ensemble-based machine learning methods 
(Random Forest and XGBoost) can effectively model complex environmental 
interactions driving pasture growth.

Feature engineering (e.g., temperature range and month-based averages) 
significantly enhanced model accuracy and interpretability.

The developed models can support agricultural management decisions 
by providing insights into the environmental factors most influential 
to pasture productivity in Queensland.


--------------------------------------------------------------
AUTHOR INFORMATION
--------------------------------------------------------------
Varun Vikas Jaiswal
Student ID: N11736089
Queensland University of Technology (QUT)
Unit: IFN703 - Advanced Data Analytics
Year: 2025


--------------------------------------------------------------
KEYWORDS
--------------------------------------------------------------
Pasture Growth, Machine Learning, Random Forest, XGBoost, 
TSDM Prediction, Feature Engineering, Environmental Analytics, 
Agricultural Data Science, Queensland, Data-driven Agriculture
