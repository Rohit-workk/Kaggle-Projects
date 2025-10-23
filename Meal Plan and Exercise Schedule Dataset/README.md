# Meal Plan and Exercise Schedule Dataset - Project Overview and Approach

---

## 📂 Dataset  
Dataset source: [Meal Plan and Exercise Schedule Dataset - Kaggle](https://www.kaggle.com/datasets/kavindavimukthi/meal-plan-and-exercise-schedule-gender-goal-bmi)  
- Samples: 80,000  
- Features: 5 categorical columns including Gender, Goal, BMI Category, Exercise Schedule, and Meal Plan

---

## 🔍 Exploratory Data Analysis (EDA)  
- Dataset contains balanced classes for Gender and Goal (muscle gain, fat burn).  
- BMI categories distributed roughly evenly among Underweight, Normal, Overweight, and Obesity.  
- Exercise Schedule and Meal Plan features have clear categorical distributions mapped to simplified labels for analysis.  
- Visualized relationships showing:
  - Correlations between BMI category and exercise intensity (e.g., Underweight → Light Exercise, Overweight → High Intensity Exercise).
  - Meal Plan preferences linked with exercise types (e.g., High Calorie Protein Diet often paired with Light Exercise).
  - Gender and Goal influencing exercise and diet patterns.

---

## 🧠 Feature Engineering  
- Simplified long exercise and meal descriptions into categorical labels for clarity and modeling ease.  
- Applied one-hot encoding to categorical features for machine learning compatibility.  
- Label encoded target variables (Meal Plan, Exercise Schedule) during separate modeling phases.

---

## ⚙️ Modeling and Evaluation  
- Trained classifiers (Logistic Regression, Decision Tree, Random Forest, AdaBoost, Bagging, KNN) to predict:
  - **Meal Plan:** Achieved perfect accuracy (1.0) across all models, indicating clearly separable classes.  
  - **Exercise Schedule:** Similarly, all models achieved perfect accuracy (1.0), reflecting clear patterns in categorical predictors.

---

## 🔍 Key Observations  
- Strong correspondence between exercise intensity, BMI, and meal preferences naturally segment the data, enabling high model accuracy.  
- Exercise Schedule and Meal Plan are highly predictable given Goal, BMI, and Gender features.  
- Predictive modeling benefits greatly from clear categorical encoding and careful feature simplification.

---

## 🔮 Conclusion & Next Steps  
- The dataset's distinct groupings make classification straightforward with simple models achieving perfect results.  
- Further exploration could focus on recommendation systems integrating nutrition and fitness plans tailored to more nuanced personal data.  
- Study the impact of external features like physical activity tracking or dietary adherence for real-world deployment.

---

## 📌 Usage  
- The project leverages Python data science stack including pandas, scikit-learn, matplotlib, and seaborn.  
- Pipeline designed for efficient handling and conversion of rich categorical health and fitness data.

---
