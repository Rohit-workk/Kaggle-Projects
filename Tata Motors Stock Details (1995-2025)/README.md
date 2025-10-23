# Tata Motors Stock Details (1995-2025) - Project Overview and Approach

---

## 📂 Dataset  
Dataset source: [Tata Motors Stock Details - Kaggle](https://www.kaggle.com/datasets/jatinkalra17/tata-motors-stock-details1995-2025)  
- Records: 7,804 daily trading entries  
- Features: 15 (dates, OHLC prices, volume, technical indicators, and trading statistics)

---

## 🔍 Exploratory Data Analysis (EDA)  
- Data covers daily stock details spanning 1995 to 2025 for Tata Motors on NSE.  
- Checked for missing values; notable missingness found in `Trades` column from 1995-2011, and minor missing values in moving averages for early years.  
- Date column converted to datetime; dataset ordered chronologically for time series analysis.  
- Visualized distributions of key numerical variables (Open, High, Low, Close, Volume, Turnover, VWAP) via histograms and boxplots revealing skewness and outliers typical of financial time series.  
- Time series plots display price and volume trends with seasonal and long-term patterns evident.  
- Correlation heatmap identifies strong interdependencies among OHLC variables, volume, and technical indicators.

---

## 🧠 Modeling Approach  
- Handled missing data by dropping rows missing critical features like Trades, MA_20, and MA_50.  
- Standard scaled numerical features to ensure uniform scale for learning algorithms.  
- Split dataset into training and test sets preserving temporal order for realistic evaluation.  
- Applied regression models: Linear Regression, Ridge, Lasso, ElasticNet, Decision Tree, Random Forest, Gradient Boosting, AdaBoost.  
- Best model: Gradient Boosting Regressor with an R2 score of ~0.975, accurately capturing complex stock price movements.  
- Random Forest and Linear-based models also achieved strong performance, while AdaBoost and DecisionTree lagged slightly.

---

## 📊 Key Insights and Observations  
- Market prices show expected volatility, with outliers reflecting real market shocks or extreme trading days.  
- Technical indicators such as moving averages play a significant role in predicting stock movement.  
- Ensemble regressors vastly outperform linear ones, underscoring the non-linear dynamics of financial data.  
- Missing data concentrated in early years highlights evolving data quality at exchanges historically.  
- Longitudinal data enables modeling of cyclical and momentum effects in stock price behavior.

---

## 🔮 Future Directions  
- Experiment with LSTM and other deep learning models tailored for sequential time series.  
- Incorporate additional macroeconomic indicators or sentiment data for enriched forecasting.  
- Deploy advanced feature engineering with technical indicator combinations and lag features.  
- Test models on recent market shocks for robust out-of-sample forecasting.

---

## 📌 Usage  
- Analysis conducted in Python with pandas, matplotlib, seaborn, scikit-learn.  
- Designed for execution in Jupyter or Kaggle Notebook environments.

---

Unlock meaningful investment signals and deep market understanding from this Tata Motors historical stock dataset through advanced time series modeling and feature engineering.
