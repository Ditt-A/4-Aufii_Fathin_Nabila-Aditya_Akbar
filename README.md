# Predicting Airbnb’s Optimum Price  
This project aims to predict the optimal rental price for Airbnb listings using machine learning.  
The dataset contains 134,545 listings across the United States with 89 features, covering property characteristics, host information, amenities, location details, and review metrics.

The project demonstrates a complete data science workflow: data preprocessing, exploratory data analysis, feature engineering, model development, model evaluation, and optimization.

## Project Objectives
- Predict optimal Airbnb listing prices using regression models.
- Identify key factors that influence pricing, such as location, property type, amenities, and host attributes.
- Provide data-driven pricing recommendations to improve occupancy and revenue.
- Build a robust, interpretable end-to-end pricing model.

## Repository Structure

```
Airbnb-Pricing-Model
├── Model/
│   ├── best_catboost_optuna.pkl
│   ├── best_xgboost_optuna.pkl
│   └── gradient_boosting_model.pkl
│
├── Notebook/
│   ├── EDA1.ipynb
│   ├── EDA2.ipynb
│   ├── Preprocessing(Cleaning).zip
│   ├── PreprocessingAndModeling1.ipynb
│   └── PreprocessingAndModeling2.ipynb
│
└── README.md

````

## Data Preprocessing

Key preprocessing steps include:

- Dropping 45 irrelevant columns out of 89.
- Handling missing values (reduced from 26 columns to 0).
- Removing exact duplicates.
- Detecting and treating natural and extreme outliers.
- Applying categorical encoding:
  - One-Hot Encoding
  - Target Encoding
  - Ordinal Encoding
- Applying feature scaling for selected models.

## Exploratory Data Analysis (EDA)

Key findings from EDA:

- Most listings fall below the $200 price point.
- States such as Vermont, Texas, and Los Angeles show significantly higher price averages.
- Low-rated properties often correlate with lower cleanliness and accuracy scores.
- Apartments and Houses dominate the property type distribution.
- Strong predictors include Cleaning Fee, Accommodates, Bedrooms, and several review scores.

Charts and visualizations are available in:
- `EDA1.ipynb`
- `EDA2.ipynb`

## Modeling Approach

Several regression algorithms were tested:

- Linear Regression  
- Ridge Regression  
- Decision Tree Regressor  
- Random Forest Regressor  
- Gradient Boosting Regressor  
- XGBoost Regressor  
- LightGBM Regressor  
- CatBoost Regressor  

### Optimization Techniques
- Hyperparameter tuning  
- Feature engineering  
- Feature selection using PCC, Mutual Information, and Tree-Based Importance  
- Domain knowledge filtering

## Model Performance

| Model                | MAE    | R²    | RMSE   |
|---------------------|--------|-------|--------|
| XGBoost (best)      | 42.03  | 0.69  | 74.07  |
| Gradient Boosting   | 42.07  | 0.69  | 74.41  |
| CatBoost            | 42.88  | 0.687 | 75.34  |

XGBoost achieved the best performance and generalization among all models tested.


## Conclusion

This project provides actionable pricing recommendations through machine learning and data-driven insights.
The final regression models deliver strong predictive performance and can assist property owners and rental platforms in setting competitive and fair nightly rates.

