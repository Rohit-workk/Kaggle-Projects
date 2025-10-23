# Spotify User Churn Analysis - Project Overview and Approach

---

## 📂 Dataset  
Dataset source: [Spotify Dataset for Churn Analysis - Kaggle](https://www.kaggle.com/datasets/nabihazahid/spotify-dataset-for-churn-analysis)  
- Samples: 8000 Spotify users  
- Features: 12 (mix of numerical and categorical user engagement, subscription, and behavior features)  
- Target variable: `is_churned` (binary classification of user churn: 0 = active, 1 = churned)

---

## 🎯 Problem Tackling Approach  
The main objective is to predict user churn by analyzing user listening behavior and subscription details, enabling Spotify to understand and reduce cancellations effectively.

---

## ⚙️ Data Preprocessing & Exploration  
- Loaded dataset and examined shape and data types, confirming 8000 entries and 12 features.  
- Detected categorical variables: gender, country, subscription type, device type, and offline listening status.  
- Identified numeric features such as age, listening time, songs played per day, skip rate, ads listened per week, and offline listening.  
- Checked for class imbalance revealing ~74% active users and ~26% churned users, motivating balanced metric evaluations.  
- Conducted value counts and unique categories exploration for all features.  
- Handled categorical variables with one-hot encoding for modeling.  
- Visualized feature distributions by churn status using count plots, pie charts, histograms, and KDE plots to uncover patterns.

---

## 🧠 Model Development and Performance  
- Used standard train-test split (80-20) and scaled numerical features using StandardScaler.  
- Trained multiple classification models including Logistic Regression, KNN, Decision Tree, SVC, Random Forest, Gradient Boosting, AdaBoost, and Bagging.  
- Baseline accuracies ranged from ~59% (Decision Tree) to ~75% (multiple ensembles and linear models).  
- Conducted hyperparameter tuning using GridSearchCV for each model, achieving cross-validation accuracies up to ~74% and test accuracies stabilizing near ~75%.  
- Logistic Regression, SVC, Random Forest, Gradient Boosting, and AdaBoost performed similarly well around 74-75% accuracy.  
- Tuned Decision Tree improved markedly over baseline, KNN showed modest improvement but lagged behind.  
- Simple ANN model built with two hidden dense layers achieved ~73% training accuracy across 10 epochs with consistent validation accuracy.

---

## 🔍 Key Insights  
- User engagement metrics such as listening time, songs played, and skip rate mildly correlate with churn.  
- Subscription type, device type, and offline listening status differentiate churn behavior.  
- Class imbalance addressed through appropriate metric evaluations rather than dataset balancing.  
- Several models demonstrate comparable predictive power, indicating the data’s patterns are moderately linear or separable.

---

## 🚀 Future Directions  
- Improve predictions with more detailed feature engineering like session durations or interaction terms.  
- Experiment with balancing techniques like SMOTE or weighted losses to improve minority class detection.  
- Explore time-series or sequential models exploiting user behavior over time.  
- Apply model explanation tools to provide actionable business insights.

---

## 📌 Usage  
- Implemented with Python using pandas, scikit-learn, matplotlib, seaborn, and TensorFlow/Keras.  
- Optimal to run in Kaggle notebooks or any compatible Python environment.

---
