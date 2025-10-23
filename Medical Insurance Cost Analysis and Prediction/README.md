# Medical Insurance Cost Analysis and Prediction

## 📄 Overview
This notebook explores and analyzes a dataset containing medical insurance information of individuals. The analysis includes **data exploration, visualization, feature engineering, and predictive modeling** to predict medical insurance charges based on various factors.

The dataset includes features related to demographics, lifestyle, and health:

- Age  
- Gender  
- Body Mass Index (BMI)  
- Number of children  
- Smoking status  
- Residential region  

---

## 🗂 Dataset

**File:** `insurance.csv`  
**Number of entries:** 1338  

You can download the dataset from [Kaggle](https://www.kaggle.com/datasets/mosapabdelghany/medical-insurance-cost-dataset).  

**Columns:**

- `age` – Age of primary beneficiary (int)  
- `sex` – Gender of beneficiary (male, female)  
- `bmi` – Body Mass Index, a measure of body fat based on height and weight (float)  
- `children` – Number of children covered by health insurance (int)  
- `smoker` – Smoking status of the beneficiary (yes, no)  
- `region` – Residential region in the US (northeast, northwest, southeast, southwest)  
- `charges` – Medical insurance cost billed to the beneficiary (float, target variable)  

---

## 🧰 Libraries Used

- `numpy`  
- `pandas`  
- `matplotlib`  
- `seaborn`  
- `scikit-learn`  

---

## 🔎 Data Exploration

- Checked **shape, column types, missing values**, and basic statistics.  
- Analyzed **distribution of numerical and categorical features**.  
- Explored relationships between features using **correlation and count plots**.  

**Observations:**

- Most beneficiaries are aged 18–64, with a balanced gender distribution.  
- Smoking has a significant effect on insurance charges.  
- Region, BMI, and number of children are also important factors.  
- No missing values in the dataset.  

---

## 📊 Visualization

- Distribution of `charges` using histogram.  
- Pie charts and bar plots for categorical features (`sex`, `smoker`, `region`, `children`).  
- Countplots comparing smoking status across sex and region.  
- Correlation heatmap for numerical features showing `age` and `bmi` as correlated with charges.  

---

## 🛠 Feature Engineering

- Scaled numerical features (`age`, `bmi`) using `StandardScaler`.  
- Encoded categorical features:
  - Label Encoding: `smoker`, `sex`  
  - One-Hot Encoding: `children`, `region`  
- Prepared final dataset for modeling with 15 features.  

---

## 🤖 Modeling

Regression models were trained to predict insurance charges:

| Model | R² Score |
|-------|-----------|
| Linear Regression | 0.754 |
| Ridge Regression | 0.754 |
| Lasso Regression | 0.754 |
| ElasticNet | 0.377 |
| Decision Tree Regressor | 0.737 |
| Random Forest Regressor | 0.840 |
| AdaBoost Regressor | 0.804 |
| Gradient Boosting Regressor | 0.865 |

**Key Insights:**

- Linear, Ridge, and Lasso regressions performed similarly.  
- ElasticNet underperformed compared to other models.  
- Tree-based ensemble methods (Random Forest, AdaBoost, Gradient Boosting) captured non-linear relationships better.  
- **Gradient Boosting Regressor** achieved the best performance (~86.5% R²).  

---

## ✅ Summary

- Insurance charges are influenced by age, BMI, smoking status, number of children, sex, and region.  
- Ensemble methods, particularly Gradient Boosting, outperform traditional linear regression techniques.  
- Further improvements are possible with **hyperparameter tuning** (Notebook link coming soon).  

---

## 🔮 Future Work

- Perform **hyperparameter optimization** using GridSearchCV or RandomizedSearchCV to improve model performance.  
- Explore **feature interactions** and polynomial features to capture more complex relationships.  
- Experiment with **advanced regression models** like XGBoost, LightGBM, and CatBoost.  
- Incorporate **external data sources** (e.g., regional healthcare statistics) for more accurate predictions.  
- Develop a **web-based application** to predict insurance charges for real-time use.  

---

## 🙏 Acknowledgment

Thank you for exploring this notebook. Insights from this analysis can help understand factors affecting medical insurance costs and improve cost prediction.  

**Keep exploring, keep learning, and happy Kaggle-ing! 🚀**
