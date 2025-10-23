# Fitness Classification Dataset Synthetic - Project Overview and Approach

---

## 📂 Dataset
Dataset used: [Fitness Classification Dataset - Kaggle](https://www.kaggle.com/datasets/muhammedderric/fitness-classification-dataset-synthetic)  
- Total samples: 2000  
- Features: 11 (including numerical and categorical)  
- Target: `is_fit` (binary classification indicating fitness status)

---

## 🔍 Data Overview
- Features include age, height, weight, heart rate, blood pressure, sleep hours, nutrition quality, activity index, smoking status, gender, and fitness label.  
- The dataset contains some missing values in `sleep_hours` which were imputed with the mean value.  
- Categorical features such as `smokes` and `gender` were encoded for modeling.

---

## ⚙️ Data Exploration & Feature Engineering
- Conducted thorough descriptive statistics and null value analysis.  
- Transformed categorical variables:  
  - Converted `smokes` from text (yes/no) to binary (1/0).  
  - Applied one-hot encoding to `gender`.  
- Dealt with outliers in numerical columns (`weight_kg`, `heart_rate`, `blood_pressure`, `sleep_hours`) using capping at 1st and 99th percentiles.  
- Visualized distributions, boxplots, countplots, and pie charts for all features and target.

---

## 🧠 Modeling Approach
- Split data into train (80%) and test (20%) sets.  
- Scaled features using StandardScaler.  
- Evaluated multiple classification models including Logistic Regression, Decision Tree, Random Forest, AdaBoost, Bagging, Voting Classifier, and KNN.  
- Logistic Regression achieved the highest accuracy (~81.25%) among all baseline models.

---

## 🔧 Hyperparameter Tuning  
- Performed GridSearchCV tuning for Random Forest, AdaBoost, Bagging, and Decision Tree.  
- Best parameters improved model effectiveness marginally:  
  - Random Forest: max_depth=5, n_estimators=70, oob_score=True  
  - AdaBoost: learning_rate=0.1, n_estimators=200  
  - Bagging: bootstrap=True, n_estimators=1000  
  - Decision Tree: criterion='gini', max_depth=2  

---

## 📊 Results & Insights  
- Ensemble methods such as Random Forest and Bagging consistently outperformed single trees and boosting methods in accuracy and stability.  
- Tuning helped improve AdaBoost and Bagging performance notably.  
- Voting Classifier combining Logistic Regression, Decision Tree, and KNN performed reasonably well but didn’t surpass Logistic Regression alone.  
- Indicates linear separability of data and effectiveness of simpler linear models in this dataset.

---

## 🔮 Conclusion and Future Work  
- Demonstrated a comprehensive workflow covering EDA, feature engineering, modeling, and tuning for fitness classification.  
- Potential improvements:  
  - Feature interactions and polynomial features for enhanced model expressiveness.  
  - Trying deep learning or more complex ensembles like XGBoost.  
  - Cross-validation with additional metrics for robust evaluation.  
  - Handling slight data imbalance with resampling or class weights.

---

## 📌 Usage  
- Implemented in Python using pandas, scikit-learn, matplotlib, and seaborn.  
- Ideal for Kaggle notebook environments with typical ML tooling.

---
