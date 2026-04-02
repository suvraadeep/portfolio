---
title: "Explainable Credit Risk Modeling"
excerpt: "An end-to-end ML system for credit risk prediction using alternative data, NLP embeddings, ensemble models, and real-time concept drift detection with explainable AI."
collection: portfolio
---

🔗 **GitHub Repo:** [Explainable Credit Risk Modeling](https://github.com/suvraadeep/Explainable-Credit-Risk-Modeling-with-Schduling)  


### Key Features:
1. **Hybrid Feature Engineering**: Combines 200+ features from 7 relational tables with NLP embeddings (Sentence-BERT).
2. **Ensemble Modeling**: LightGBM + XGBoost with Optuna hyperparameter tuning and 5-fold CV.
3. **Explainability (SHAP)**: Full interpretability with beeswarm, waterfall, and dependence plots.
4. **Concept Drift Detection**: Real-time drift monitoring using River's ADWIN with auto-retraining.
5. **Interactive Dashboard**: Streamlit app for live scoring, explanations, and drift simulation. :contentReference[oaicite:0]{index=0}  


### Example Workflow:
#### Input: *Applicant financial data*
1. **Feature Engineering**:
   - Generates tabular + NLP features.
2. **Prediction**:
   - Ensemble model computes default probability.
3. **Explainability**:
   - SHAP explains top contributing factors.

#### Scenario: *Economic shock (income drop)*
1. **Drift Simulation**:
   - Applies synthetic distribution shift.
2. **Detection**:
   - ADWIN detects drift in real-time.
3. **Adaptation**:
   - Model retrains for updated distribution.




### Technologies Used:
- **Python (Pandas, NumPy)**: Data processing and feature engineering.
- **LightGBM & XGBoost**: Ensemble modeling.
- **Optuna**: Hyperparameter optimization.
- **Sentence-BERT**: NLP embeddings.
- **SHAP**: Model explainability.
- **River (ADWIN)**: Online drift detection.
- **Streamlit**: Interactive dashboard.
