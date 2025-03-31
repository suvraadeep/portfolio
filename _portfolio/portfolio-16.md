---
title: "BrisT1D-AutoGlucon Ensemble"
excerpt: "This project leverages AutoGluon, an automated machine learning library, to predict blood glucose levels (bg+1:00) for diabetic patients using the BrisT1D dataset. The pipeline includes preprocessing, feature engineering, and training ensemble models with dynamic stacking. The best-performing model achieves a Root Mean Squared Error (RMSE) of 1.99 using weighted ensemble techniques."
collection: portfolio
---

🔗 **Notebook Link:** [BrisT1D-AutoGlucon Ensemble](https://www.kaggle.com/code/suvroo/brist1d-autoglucon-ensemble-baseline)  


## Overview
This notebook demonstrates the use of **AutoGluon** to predict blood glucose levels (`bg+1:00`) for Type 1 Diabetes patients based on historical data and activity features from the **BrisT1D dataset**. The workflow includes data preprocessing, feature engineering, model training, and evaluation using advanced ensemble methods.

---

## Dataset Information
- **Source**: BrisT1D Dataset
- **Train Shape**: `(177024, 508)`
- **Test Shape**: `(3644, 507)`
- **Target Variable**: `bg+1:00` (blood glucose level after 1 hour)
- **Features**:
  - Historical blood glucose readings (`bg-*`)
  - Insulin intake (`insulin-*`)
  - Carbohydrate consumption (`carbs-*`)
  - Heart rate (`hr-*`)
  - Activity levels (`activity-*`)
  - Time-based features (`hour`, `minute`)

---

## Tech Stack
- **Python**: Core programming language.
- **Pandas & NumPy**: For data manipulation and preprocessing.
- **AutoGluon.Tabular**: Automated machine learning framework for regression tasks.
- **Ray**: For distributed computing (optional).
- **Matplotlib & Seaborn**: For data visualization.

---

## Features

### Data Preprocessing
1. Handles mixed data types and missing values.
2. Extracts time-based features (`hour`, `minute`) from timestamps.
3. Removes irrelevant columns (e.g., `id`).

### Model Training
1. Uses AutoGluon's TabularPredictor for regression tasks.
2. Applies dynamic stacking with multi-layer ensembles (up to 5 levels).
3. Hyperparameter tuning includes:
   - Neural networks with PyTorch backend (`NN_TORCH`).
   - Gradient Boosting (`LightGBM`).

### Evaluation Metrics
- Root Mean Squared Error (RMSE): Used to evaluate model performance.
- Validation RMSE of the best model: **1.99**

### Predictions
Generates predictions for test data and saves results in CSV files for submission.

## Results
```python
| Model                  | Validation RMSE | Stack Level |
|------------------------|-----------------|-------------|
| WeightedEnsemble_L5    | **1.99**        | 5           |
| NeuralNetTorch_BAG_L2  | 2.00            | 2           |
| LightGBM_BAG_L4        | 2.11            | 4           |
```



## Key Insights

1. **Dynamic Stacking**:
   - Multi-layer stacking improves predictive performance by reducing overfitting.
   - Weighted ensembles outperform individual models.

2. **Feature Importance**:
   - Historical blood glucose levels (`bg-*`) are the most significant predictors.
   - Activity levels and insulin intake contribute marginally.

3. **Model Performance**:
   - Ensemble models achieve better RMSE than standalone models like LightGBM or NeuralNetTorch.


