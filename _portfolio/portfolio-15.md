---
title: "XGB :Indian Metropolitian City Rent Prediction"
excerpt: "This project focuses on predicting rental prices in major Indian cities using machine learning regression models. The dataset consists of 4700+ properties with features like BHK, rent, size, furnishing status, tenant preferences, and more. The notebook explores data preprocessing, feature engineering, and model evaluation using algorithms such as Linear Regression, Gradient Boosting, and XGBoost, with hyperparameter tuning via Optuna. Ensemble methods like bagging are also applied to address overfitting and improve model performance."
collection: portfolio
---

🔗 **Notebook Link:** [XGB :Indian Metropolitian City Rent Prediction](https://www.kaggle.com/code/suvroo/xgb-indian-metropolitian-city-rent-prediction)  



## Overview
This project aims to predict rental prices for houses and apartments in top-tier Indian cities using a structured machine learning pipeline. The dataset includes detailed property features, and the workflow involves preprocessing, feature engineering, model selection, hyperparameter tuning, and evaluation.


## Dataset Information
- **Dataset Size**: 4700+ records
- **Features**:
  - `BHK`: Number of bedrooms, hall, kitchen.
  - `Rent`: Target variable (monthly rent in INR).
  - `Size`: Area in square feet.
  - `Furnishing Status`: Furnished, Semi-Furnished, or Unfurnished.
  - `Tenant Preferred`: Type of tenant (e.g., Bachelors/Family).
  - `City`: Location of the property (e.g., Mumbai, Bangalore).
  - Additional features include `Bathrooms`, `Floor`, and `Area Type`.


## Tech Stack
- **Python**: Core programming language.
- **Pandas & NumPy**: For data manipulation and preprocessing.
- **Sklearn**: For model training and evaluation.
- **XGBoost & LightGBM**: For advanced boosting techniques.
- **Optuna**: For hyperparameter optimization.
- **Plotly & Matplotlib**: For data visualization.


## Workflow

### 1. Data Preprocessing
- Extracted numerical features from categorical columns (e.g., `Floor` → `CurrentFloor` and `TotalFloors`).
- Handled missing values using KNN Imputation.
- Converted categorical variables to numerical using Label Encoding.
- Removed outliers using the IQR method.

### 2. Exploratory Data Analysis (EDA)
- Visualized relationships between features like `City`, `Furnishing Status`, and `Rent`.
- Identified patterns such as:
  - Higher rents in Mumbai compared to other cities.
  - Unfurnished properties generally have lower rents.

### 3. Feature Engineering
- Created additional features like year extracted from the date column (`Posted On`).
- Dropped less important features based on correlation analysis.

### 4. Model Selection
- Evaluated multiple regression models:
  - Linear Regression
  - Ridge & Lasso Regression
  - Gradient Boosting Regressor
  - Random Forest Regressor
  - XGBoost & LightGBM
- Compared models using R² scores for both training and test sets.

### 5. Hyperparameter Tuning with Optuna
- Optimized XGBoost parameters such as:
  - Learning rate
  - Max depth
  - Subsample ratio
- Achieved the best RMSE of **6790.75** on the test set.

### 6. Ensemble Methods
- Applied bagging techniques to reduce overfitting.
- Used GridSearchCV to find the best parameters for Bagging Regressors.



## Results
```bash
| Model                  | Train R² | Test R² |
|------------------------|----------|---------|
| Linear Regression      | 0.65     | 0.62    |
| Random Forest          | 0.92     | 0.74    |
| XGBoost (Tuned)        | 0.97     | 0.77    |
| Bagging Regressor      | 0.88     | 0.76    |
```

## Key Insights
1. Mumbai has the highest rental prices due to high demand.
2. Unfurnished properties are more affordable compared to semi-furnished or furnished ones.
3. Larger properties (higher BHK) generally have higher rents but with diminishing returns for very large properties.






