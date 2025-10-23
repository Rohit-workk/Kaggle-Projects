# 🩺 Medical Insurance Cost Prediction & Health Risk Analysis

## 🧠 Overview
This project performs an end-to-end analysis and prediction of **medical insurance costs** and **health risk scores** using an extensive dataset of over **100,000 patient records** and **54 features**.  
The goal is to understand how **demographic, socioeconomic, and lifestyle factors** influence health risks and insurance expenditures, and to build predictive machine learning models for accurate estimation.

---

## 🎯 Objectives
- Analyze key features that affect medical cost and health risk.  
- Conduct an in-depth **exploratory data analysis (EDA)**.  
- Implement and compare multiple regression and ensemble models.  
- Predict **risk scores** and **annual medical costs** effectively.  

---

## 📂 Dataset Information
Dataset used: [Medical Insurance Cost Prediction – Kaggle](https://www.kaggle.com/datasets/mohankrishnathalla/medical-insurance-cost-prediction)  

**Shape:** 100,000 rows × 54 columns  

### Feature Categories
- **Demographic:** age, sex, region, urban/rural, marital status, education.  
- **Socioeconomic:** income, employment status, household size, dependents.  
- **Lifestyle:** BMI, smoker, alcohol frequency.  
- **Medical History:** chronic diseases (hypertension, diabetes, arthritis, etc.).  
- **Healthcare Utilization:** hospital visits, procedures, consultations.  
- **Insurance:** plan type, deductible, copay, term period, premium details.  
- **Target Columns:** `risk_score`, `annual_medical_cost`, `is_high_risk`.

### Data Quality
- The dataset is clean and well-structured.  
- Only one column (`alcoholfreq`) had missing values (≈30.08%).  

---

## 🔍 Exploratory Data Analysis (EDA)

### Key Observations
- **Age & Risk:** Increasing age correlates strongly with higher `risk_score`.  
- **Chronic Diseases:** Higher `chroniccount`, `systolicbp`, and `bmi` relate to higher medical risks.  
- **Lifestyle:** Smokers show higher `risk_score`, `annual_medical_cost`, and `claimscount`.  
- **Socioeconomic Distribution:** Urban and high-income individuals exhibit higher healthcare utilization and insurance premiums.  
- **Insurance Patterns:** Premiums, copay, and deductible levels directly influence yearly costs.

### Correlation with Risk Score
| Feature               | Correlation |
|------------------------|-------------|
| is_high_risk           | 0.821 |
| age                    | 0.721 |
| chroniccount           | 0.666 |
| systolicbp             | 0.554 |
| smoker_Current         | 0.322 |
| diabetes               | 0.234 |
| mentalhealth           | 0.285 |
| cardiovascular_disease | 0.193 |

---

## 🧩 Feature Engineering
- One-hot encoded all categorical features.  
- Scaled continuous variables using `StandardScaler`.  
- Training and test split (80% training, 20% testing).  

---

## ⚙️ Machine Learning Models

| Model | R² Score | Comment |
|--------|-----------|----------|
| Linear Regression | 0.9694 | Strong linear relationship |
| Ridge Regression | 0.9695 | Stable and consistent |
| Lasso Regression | -0.00005 | Over-regularized, underfit |
| ElasticNet | -0.00005 | Underfit, high penalty |
| Decision Tree | 0.99997 | Extremely high fit (possible overfitting) |
| Random Forest | 0.99997 | Excellent, needs validation |
| Gradient Boosting | 0.9911 | Strong balance and accuracy |
| AdaBoost | 0.8727 | Moderate success |

---

## 🧠 EDA Conclusion
The analysis demonstrates that **age**, **chronic diseases**, and **lifestyle choices** (like smoking) are the dominant drivers of health risk and cost prediction.  
Patients with chronic illnesses and poor lifestyle indicators consistently show **higher annual medical expenses** and **higher health risk scores**.

Tree-based ensemble models (**Random Forest, Decision Tree**) achieved nearly perfect R² values (~0.9999), suggesting overfitting potential that must be validated further.  
**Gradient Boosting** offered the best mix of high accuracy (~0.9911) and generalization capability.  
In contrast, **Lasso and ElasticNet** underperformed due to excessive regularization.  
The **Linear and Ridge models** effectively captured the strong linear dependencies in the dataset.

In conclusion, medical insurance cost prediction is best addressed with advanced ensemble methods and thorough feature scaling.  
The findings highlight that preventive care and lifestyle modifications could reduce both risk and cost burdens significantly.

---

## 🧰 Tech Stack
- **Language:** Python  
- **Libraries:** pandas, numpy, matplotlib, seaborn, scikit-learn  
- **Models Used:** Linear, Ridge, Lasso, ElasticNet, Decision Tree, Random Forest, Gradient Boosting, AdaBoost  
- **Environment:** Jupyter Notebook / Kaggle Notebook  

---

## 🚀 Future Improvements
- Add **hyperparameter tuning** (GridSearchCV).  
- Apply **cross-validation** for generalization.  
- Explore **XGBoost** and **LightGBM**.  
- Deploy the final model with **Streamlit or Flask** for live prediction.  

---

## 💡 Final Thoughts
This project illustrates how effective **EDA + ML modeling** can uncover meaningful insights about healthcare costs and risk factors.  
By leveraging statistical analysis and machine learning, the notebook supports smarter **insurance pricing**, **health policy design**, and **patient risk management**.
