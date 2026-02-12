# HSN Code 8482 – Import & Export Forecasting (2014–2026)

## 📌 Project Overview
This project develops a time-series forecasting model for trade flows of **HSN Code 8482 (Ball & Roller Bearings)** in India.

The objective is to:
- Analyze historical trade data (2014–2024)
- Forecast import and export values for 2025–2026
- Evaluate predictive performance using statistical error metrics

---

## 📊 Dataset Information
- Period Covered: 2014–2024  
- Trade Flows:
  - Imports (M)
  - Exports (X)
- Metric Used: Trade Value (US$)

---

## 🧠 Methodology

### Data Preparation
- Converted trade values into numeric format
- Mapped trade flows (M → Imports, X → Exports)
- Created yearly pivot table for modeling

### Modeling Approach

**Imports Model**
- ARIMA (1,1,1)

**Exports Model**
- ARIMAX (1,1,1)
- Imports used as an exogenous variable

### Evaluation Metrics
- MAE (Mean Absolute Error)
- RMSE (Root Mean Squared Error)

---

## 📊 Model Performance

### Imports – ARIMA (1,1,1)
- MAE: 70,663,385.29
- RMSE: 79,375,737.08

| Year | Actual (US$) | Predicted (US$) | Error |
|------|--------------|----------------|--------|
| 2023 | 1,329,567,039 | 1,295,058,786 | 2.60% |
| 2024 | 1,400,087,595 | 1,293,269,077 | 7.63% |

### Exports – ARIMAX (1,1,1)
- MAE: 73,209,916.56
- RMSE: 88,569,896.68

| Year | Actual (US$) | Predicted (US$) | Error |
|------|--------------|----------------|--------|
| 2023 | 783,726,023 | 807,086,820 | 2.98% |
| 2024 | 753,998,896 | 877,057,932 | 16.32% |

---

## 🔮 Forecast Results (2025–2026)

### Imports Forecast
| Year | Forecast (US$) |
|------|----------------|
| 2025 | 1,293,053,838 |
| 2026 | 1,293,027,952 |

### Exports Forecast
| Year | Forecast (US$) |
|------|----------------|
| 2025 | 787,331,237 |
| 2026 | 819,132,972 |

---

## 📈 Forecast Visualization

![Forecast Plot](images/hsn_8482_forecast.png)

---

## 🛠️ Technologies Used
- Python
- Pandas
- NumPy
- Matplotlib
- Statsmodels
- Scikit-learn
- Jupyter Notebook

---

## 🚀 How to Run This Project

1. Install dependencies:
pip install -r requirements.txt
2. Launch Jupyter Notebook:
jupyter notebook


3. Open:
notebooks/HSNCode.ipynb


---

## 📌 Key Insights
- Imports are projected to remain stable around 1.29B US$
- Exports show moderate growth from 2025 to 2026
- ARIMAX improves export forecasting by incorporating import trends
- Model accuracy ranges between 2–16% error

---

## 📄 License
This project is developed for academic and analytical purposes.