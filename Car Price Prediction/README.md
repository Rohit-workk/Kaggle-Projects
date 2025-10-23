# Used Car Price Prediction - Project Overview and Approach

---

## 📂 Dataset  
Dataset used: [Used Car Price Prediction - Kaggle](https://www.kaggle.com/datasets/vrajesh0sharma7/used-car-price-prediction)  
- Samples: 7401  
- Features: 29 (including categorical and numerical car attributes, sale information, and price)  
- Target variable: `saleprice` (price of the used car)

---

## 🔍 Data Understanding  
- Dataset contains information about car brand, model year, fuel type, kilometers run, city, transmission, car rating, owners, broker quote, EMI details, and warranty among others.  
- Mixed data types with both numerical and categorical features.  
- Missing values replaced with meaningful categories like "noclass" or "nowork" for categorical variables.  
- Extracted car brand from model name for better categorical analysis.

---

## ⚙️ Exploratory Data Analysis  
- Count and distribution plots reveal:
  - Most cars manufactured in years 2015-2017, with a peak at 849 cars in 2015.  
  - Popular brands such as Maruti (3179 cars), Hyundai (1800), Honda (592), and Toyota (365) dominate the dataset.  
  - Brand-wise analysis shows distinct trends in fuel types, body types, ownership counts, transmissions, and city-wise sales distribution.  
- Numerical features like EMI start amount, booking down payment, and sale price are visualized via boxplots and bar charts segmented by brand frequency categories (high, medium, low).  
- Warranty, fitness certificate availability, and reserved status vary significantly among premium and common brands.

---

## 🧩 Feature Engineering  
- Extracted brand names from car model strings using regex and handling multi-word brand names.  
- Categorized brands by frequency: high, medium, and low to simplify analysis.  
- Created pivot tables and plotted distributions for categorical features by brand frequency to reveal feature-brand relationships.

---

## 📊 Statistical Summary and Feature Insights:

### Key Numerical Features:

| Feature             | Mean       | Median | Min   | Max        | Std Dev     |
|---------------------|------------|--------|-------|------------|-------------|
| `saleprice`         | 365,586.31 | NA     | 10,000| 9,948,900  | ~445,108.7  |
| `kmsrun`            | 29,980     | NA     | 0     | 366,000    | ~33,904     |
| `emi_starts_from`   | 11,091.2   | NA     | 0     | 42,837     | NA          |
| `booking_down_pymnt`| 63,567.54  | NA     | 0     | 500,000    | NA          |

### Year of Manufacture Trends:
- Manufactured cars are predominantly from 2015 to 2017, tapering off in other years.
- Hatchbacks and manual transmission cars dominate.

### Brand Distributions:
- High-frequency brands strongly impact sales and price trends.
- Premium brands command higher average sale prices, EMIs, and booking amounts.

### Feature Observations:
- Fuel and transmission types correlate with brand segmentation.
- Warranty and fitness certificates are more prevalent in premium brands, potentially influencing price.

---

## 🔮 Key Insights & Next Steps  
- Brand and year of manufacture are critical influencers on price.  
- Feature engineering focused on brand extraction and frequency categorization lends better interpretability and model readiness.  
- Next steps include predictive modeling with ensemble regressors, feature importance analysis, and potential market segmentation clustering.

---

## 📌 Usage  
- Developed using Python with pandas, matplotlib, seaborn, and regex.  
- Designed for Kaggle kernels or Jupyter environments with similar configurations.

---
