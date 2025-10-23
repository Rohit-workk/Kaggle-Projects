# Dhaka Air Quality Dataset (2000-2025) - Project Overview and Approach

---

## 📂 Dataset  
Dataset source: [Dhaka Air Quality 2000-2025 Synthetic Dataset - Kaggle](https://www.kaggle.com/datasets/shakil10945/dhaka-air-quality-2000-2025-synthetic-dataset)  
- Records: 225,816  
- Features: 12 (including timestamp and multiple air quality indicators and meteorological variables)  
- Target focus: Air Quality Index (AQI)

---

## 🔍 Data Understanding  
- The dataset contains hourly air quality measurements from 2000 to 2025 for Dhaka city, including pollutants such as PM2.5, PM10, O3, NO2, SO2, CO and environmental variables like temperature, humidity, wind speed, and pressure.  
- No missing values reported; well-structured with timestamp in datetime format.  
- Pollutant and environmental features are numerical with varying distributions and ranges.

---

## ⚙️ Exploratory Data Analysis  

### Summary Statistics for Numerical Features:

| Feature      | Mean  | Std Dev | Min | 25th Percentile | Median | 75th Percentile | Max   |
|--------------|-------|---------|-----|-----------------|--------|-----------------|-------|
| AQI          | 173.88| 47.85   |20.83| 153.49          |171.49  |194.74           |299.60 |
| PM2.5        | 105.49| 55.87   |5.00 | 62.13           | 96.29  |140.41           |250.00 |
| PM10         | 178.66| 95.03   |10.00| 105.42          |164.38  |240.08           |400.00 |
| O3           | 50.07 | 18.18   |5.00 | 37.13           | 48.39  | 61.14           |124.49 |
| NO2          | 34.29 | 12.19   |5.00 | 25.62           | 33.78  | 42.60           |87.30  |
| SO2          | 23.08 | 7.69    |2.00 | 17.72           | 22.48  | 27.79           |57.27  |
| CO           | 1.64  | 0.53    |0.10 | 1.25            | 1.61   | 2.01            |3.76   |
| Temperature  | 26.04 | 5.14    |10.34| 22.08           | 26.06  | 29.99           |40.00  |
| Humidity     | 70.02 | 10.62   |30.00| 62.33           | 69.34  | 77.49           |95.00  |
| WindSpeed    | 12.99 | 4.94    |8.00 | 9.44            | 11.47  | 14.94           |40.00  |
| Pressure     |1012.95| 7.86    |990.00|1007.62          |1012.99 |1018.40          |1030.00|

### AQI Categories  
- Categorized hourly AQI into standard categories: Good, Moderate, Unhealthy for Sensitive, Unhealthy, Very Unhealthy, Hazardous.  
- Yearly and monthly analysis of AQI categories shows increasing pollutant levels over time with variability across months and times of day.

### Outlier Analysis  
- Outliers detected in AQI and some pollutant measures likely reflect real pollution events, not measurement errors.  
- No data censoring applied to preserve genuine environmental spikes.

---

## 📊 Temporal Trends and Visualization
- Yearly averages, max, and min for pollutants show increasing trends in AQI and particulate matter from 2000 to 2025.  
- Monthly and hourly trends highlight seasonal and diurnal variations, with pollutant peaks in specific months and times of day consistent with weather and human activities.  
- Heatmaps and correlation matrix reveal strong correlations between AQI and particulate matter (PM2.5, PM10), moderate correlations with NO2 and CO.

---

## 🧠 Modeling Approach and Performance

### Regression Models evaluated to predict AQI:

| Model                  | R2 Score  | Notes                                  |
|------------------------|-----------|---------------------------------------|
| Linear Regression      | 0.9323    | Good fit, but linear limitations       |
| Ridge Regression       | 0.9323    | Similar to Linear, regularization helps|
| Lasso Regression       | 0.9322    | Slightly lower, feature selection effect|
| ElasticNet             | 0.9322    | Combination of L1 and L2 effects       |
| Random Forest Regressor| 0.9999999 | Extremely accurate capturing non-linear relationships |
| Gradient Boosting      | 0.999907  | High accuracy with non-linear modeling|
| AdaBoost Regressor     | 0.99397   | High accuracy, less prone to overfit   |
| Decision Tree          | 0.9999999 | Very high but may overfit               |

- Tree-based ensemble models (Random Forest, Gradient Boosting) outperform linear models significantly in capturing complex air pollution patterns.  
- High R2 values near 1 indicate excellent fit, but careful validation needed to prevent overfitting.

---

## 🔮 Future Work Recommendations  
- Perform time-series modeling using ARIMA, SARIMA, or LSTM to forecast AQI based on temporal patterns.  
- Optimize tree-based models with hyperparameter tuning to improve generalization.  
- Investigate seasonal and event-driven pollution spikes for intervention planning.  
- Develop a real-time AQI prediction and alert system for Dhaka city.

---

## 📌 Usage  
- The analysis is implemented in Python using pandas, matplotlib, seaborn, scikit-learn.  
- Kaggle Notebook environment is recommended for reproducibility.

---
