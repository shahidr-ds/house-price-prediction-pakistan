# 🏠 House Price Prediction in Pakistan

This project predicts residential house prices in Pakistan using real estate listings and machine learning techniques like Linear Regression, Random Forest, and XGBoost. The workflow includes advanced feature engineering, outlier handling, model tuning, and SHAP-based model interpretation.

---

## 📁 Dataset Overview

- **Dataset Name:** Pakistan House Prices  
- **Format:** CSV  
- **Source:** *(Private dataset — replace with link if public)*  
- **Size:** ~10,000 rows, 15+ features  
- **Attributes:** Location, Property Type, Area, Bedrooms, Bathrooms, Date Listed, Latitude/Longitude, etc.

---

## 🧠 ML Workflow

1. **Data Cleaning**: Remove non-informative columns, handle missing values
2. **Feature Engineering**:
   - Date-based fields (month, weekday, etc.)
   - Log transformations to reduce skew
   - Distance to city center (using lat/lon)
   - Room ratios (bed/bath per area)
   - KMeans clustering (location-based grouping)
3. **EDA & Visualization**:
   - Outlier detection (IQR method)
   - Distribution plots, boxplots, and heatmaps
4. **Modeling**:
   - Linear Regression
   - Random Forest Regressor
   - XGBoost Regressor (with GridSearchCV tuning)
5. **Evaluation**:
   - R² Score, MAE, RMSE
   - Residual analysis
   - SHAP plots for feature importance and model transparency

---

## ✅ Results

| Model              | R² Score | MAE     | RMSE    |
|--------------------|----------|---------|---------|
| Linear Regression  | 0.8277   | 0.1780  | 0.4401  |
| Random Forest      | 0.9927   | 0.0075  | 0.0903  |
| XGBoost (Tuned)    | 0.9686   | 0.0331  | 0.1879  |

---

## 📂 Repository Structure

```bash
.
├── notebooks/
│   └── House_Price_Prediction_Pakistan_Final.ipynb  # Main analysis notebook
├── data/
│   └── pakistan_house_price_data.csv                # Dataset (not included if private)
├── models/
│   └── xgboost_house_price_model.pkl                # Saved best model
├── images/
│   └── shap_summary.png                             # Optional for README
├── README.md                                        # Project documentation
└── requirements.txt                                 # Libraries used
