# Academic Stress Level Analysis and Prediction

## 📄 Overview
This notebook explores and analyzes a dataset capturing students' academic stress levels through survey responses. The dataset includes information on:

- Peer pressure
- Academic pressure from home
- Study environment
- Coping strategies
- Personal habits
- Academic competition

The notebook performs **data exploration, visualization, feature engineering, and predictive modeling** to understand factors influencing academic stress among students.

---

## 🗂 Dataset

**File:** `academic Stress level - maintainance 1.csv`  
**Number of entries:** 140  

**Columns:**

- `Timestamp` – Survey timestamp  
- `Your Academic Stage` – Student's education stage  
- `Peer pressure` – Level of peer pressure (1–5)  
- `Academic pressure from your home` – Home-related academic pressure (1–5)  
- `Study Environment` – Quality of study environment  
- `What coping strategy you use as a student?` – Coping strategy  
- `Do you have any bad habits like smoking, drinking on a daily basis?` – Personal habits  
- `What would you rate the academic competition in your student life` – Perceived competition (1–5)  
- `Rate your academic stress index` – Target variable (stress level, 1–5)  

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
- Analyzed **distribution of features**, both numerical and categorical.  
- Performed **date-wise analysis** to track survey submission trends.  

**Observations:**

- Most students with higher stress levels are undergraduates.  
- Peer and home pressure positively correlate with stress.  
- Peaceful study environments reduce stress.  
- Coping strategies and bad habits influence stress levels.  
- Academic competition perception impacts stress.  

---

## 📊 Visualization

- Count plots and pie charts for categorical and numerical features.  
- Date-wise line plots to visualize survey submissions.  
- Visual comparison of stress levels across features like:
  - Academic stage  
  - Peer pressure  
  - Study environment  
  - Coping strategy  

---

## 🛠 Feature Engineering

- Dropped irrelevant timestamp columns.  
- Encoded categorical features:
  - **Label Encoding:** `bad_habbits`  
  - **Ordinal Encoding:** `acadmic_stage`  
  - **One-Hot Encoding:** `Study Environment`, `strategy_used`  

---

## 🤖 Modeling

Models trained to predict students' stress levels:

| Model | Accuracy | Observation |
|-------|---------|-------------|
| Logistic Regression | 0.357 | Linear assumptions may not capture complex relationships |
| Decision Tree | 0.464 | Handles non-linearities but may overfit |
| Random Forest | 0.357 | Low performance; may need hyperparameter tuning |
| AdaBoost | 0.643 | Best performance; boosting improves weak learners |
| Bagging | 0.393 | Slight improvement over single estimators |
| K-Nearest Neighbors | 0.321 | Distance-based struggles with categorical/high-dim data |
| SVC (RBF kernel) | 0.571 | Reasonable performance; captures non-linear boundaries |

**Key Insights:**

- Ensemble methods (AdaBoost) outperform single estimators.  
- Stress levels have non-linear relationships with features.  
- Tree-based models may improve with further tuning.  

---

## ✅ Summary

- Academic stress is influenced by **peer pressure, home environment, study environment, coping strategies, personal habits, and academic competition**.  
- Data preprocessing and feature engineering significantly impact predictive performance.  
- **AdaBoost** and **SVC** are the most promising models for predicting stress levels.  

---

## 📌 Usage

1. Load the dataset:
    ```python
    df = pd.read_csv("academic Stress level - maintainance 1.csv")
    ```
2. Perform preprocessing, visualization, and feature engineering.  
3. Train models using `scikit-learn`.  
4. Evaluate model performance with `accuracy_score`.  

---

## 🙏 Acknowledgment

Thank you for exploring this notebook. Insights from this analysis can help understand factors influencing academic stress among students and inform interventions to reduce it.  

**Keep exploring, keep learning, and happy Kaggle-ing! 🚀**
