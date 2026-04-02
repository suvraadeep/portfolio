---
title: "Cascading Crop Failure Early Warning System"
excerpt: "A multi-modal AI system for early crop stress detection using satellite NDVI, weather data, and Temporal Fusion Transformers with conformal prediction for reliable forecasting."
collection: portfolio
---

🔗 **GitHub Repo:** [Cascading Crop Failure Early Warning System](https://github.com/suvraadeep/Cascading-Crop-Failure-Early-Warning-System)  


### Key Features:
1. **Multi-Modal Forecasting**: Combines satellite NDVI, weather, and soil data for crop stress prediction.
2. **Temporal Fusion Transformer (TFT)**: Multi-horizon time-series forecasting for 21-day NDVI prediction.
3. **Conformal Prediction**: Provides statistically guaranteed uncertainty intervals (≥90% coverage).
4. **Early Warning System**: Detects crop stress 2–3 weeks in advance with actionable alerts.
5. **End-to-End Dashboard**: Streamlit app with risk visualization, weather analytics, and SMS alerts. :contentReference[oaicite:0]{index=0}  


### Example Workflow:
#### Input: *Farm location (lat/lon)*
1. **Data Pipeline**:
   - Fetches NASA POWER weather + NDVI signals.
2. **Feature Engineering**:
   - Generates 80+ temporal and domain-specific features.
3. **Prediction**:
   - TFT forecasts next 21 days NDVI.
4. **Risk Detection**:
   - Flags stress if NDVI < threshold (e.g., 0.35).

#### Scenario: *Drought / heat stress*
1. **Forecast Analysis**:
   - Detects NDVI decline trends.
2. **Uncertainty Estimation**:
   - Conformal intervals quantify prediction confidence.
3. **Alert System**:
   - Sends actionable SMS alerts to farmers.


### Screenshots:

#### Dashboard Overview
![Dashboard](https://github.com/suvraadeep/Cascading-Crop-Failure-Early-Warning-System/blob/main/utils/1.jpeg)

#### Weather & Feature Analysis
![Weather](https://github.com/suvraadeep/Cascading-Crop-Failure-Early-Warning-System/blob/main/utils/2.jpeg)

#### Regional Risk & Alerts
![Risk](https://github.com/suvraadeep/Cascading-Crop-Failure-Early-Warning-System/blob/main/utils/3.jpeg)

#### TFT Prediction Output
![TFT](https://github.com/suvraadeep/Cascading-Crop-Failure-Early-Warning-System/blob/main/crop_ews/tft_predictions.png)


### Technologies Used:
- **PyTorch Forecasting**: Temporal Fusion Transformer implementation.
- **Python (Pandas, NumPy)**: Data pipeline and feature engineering.
- **NASA POWER API**: Weather data source.
- **Conformal Prediction**: Reliable uncertainty estimation.
- **Plotly & Folium**: Interactive visualization.
- **Streamlit**: Deployment dashboard.
- **Twilio API**: SMS alert system.
