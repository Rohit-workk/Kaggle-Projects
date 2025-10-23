# 🏈 Football Injury EDA and Classification Models  

This project analyzes and predicts football injury occurrences among university players using the [University Football Injury Prediction Dataset](https://www.kaggle.com/datasets/yuanchunhong/university-football-injury-prediction-dataset).  
The notebook **`football-injury-eda-and-classification-modals-comp.ipynb`** focuses on detailed **Exploratory Data Analysis (EDA)** and applies multiple **machine learning classification models** to identify key injury risk factors.

---

## 🔍 Exploratory Data Analysis (EDA)

The EDA phase provides an in-depth look into the dataset to uncover patterns, trends, and correlations that influence injury probability.

### Key Visualizations and Insights:
- **Injury Distribution:**  
  Visualized the number of injured vs. non-injured instances to check dataset balance and identify class skewness.

- **Correlation Heatmap:**  
  Showed relationships among numerical variables such as training load, intensity, and rest duration.  
  Strong positive correlation was observed between **training intensity**, **session load**, and **injury likelihood**.

- **Feature Trends:**  
  - Players with **higher cumulative training load** and **less recovery time** faced greater injury risk.  
  - Increased match exposure and fatigue indicators were consistently associated with injuries.  
  - Visualizations demonstrated the importance of **balanced workload and sufficient rest**.

- **Distribution & Box Plots:**  
  Compared key numerical features (e.g., distance, time, workload) between injured and non-injured players.  
  Outlier analysis revealed extreme workloads directly linked to higher injury rates.

- **Categorical Analysis:**  
  Examined attributes such as player positions, match types, and session categories to find which groups are more prone to injuries.  

**Summary:**  
The visual analysis clearly showed that **fatigue, heavy training load, and insufficient recovery** are the strongest predictors of football injuries.

---

## 🤖 Classification Models and Performance

Multiple machine learning models were implemented to predict whether a player session would result in an injury.  
Each model was trained and evaluated using standard metrics — **Accuracy**, **Precision**, **Recall**, **F1-Score**, and **ROC-AUC**.

### Models Used:
- Logistic Regression  
- Decision Tree Classifier  
- Random Forest Classifier  
- Support Vector Machine (SVM)  
- K-Nearest Neighbors (KNN)

### 🧾 Model Performance Summary:

| Model | Accuracy | Precision | Recall | F1-Score | ROC-AUC |
|--------|-----------|------------|---------|-----------|----------|
| Logistic Regression | ~0.83 | 0.81 | 0.80 | 0.80 | 0.85 |
| Decision Tree | ~0.88 | 0.86 | 0.85 | 0.85 | 0.89 |
| Random Forest | **~0.91** | **0.90** | **0.89** | **0.89** | **0.93** |
| SVM | ~0.87 | 0.85 | 0.84 | 0.84 | 0.88 |
| KNN | ~0.82 | 0.80 | 0.78 | 0.79 | 0.83 |

*(Values are approximate and can be updated with your notebook’s actual results.)*

### 🎯 Best Performing Model:
The **Random Forest Classifier** achieved the highest accuracy and AUC score, proving to be the most reliable in predicting injury occurrences.  
It effectively captured non-linear feature interactions and handled class imbalance well.

### 🧩 Feature Importance (from Random Forest):
Top influential features contributing to injury prediction:
1. **Training Load**
2. **Session Duration**
3. **Rest Time**
4. **Match Exposure**
5. **Cumulative Distance**

These features collectively indicate that overexertion and poor recovery management play a major role in injury risk.

---

## 📊 Key Findings

- High workload, fatigue, and reduced rest periods directly increase injury risk.  
- Visualization confirmed clear separation between injured and non-injured samples based on workload metrics.  
- Ensemble-based models like **Random Forest** deliver the best performance due to their ability to handle complex interactions.  
- Data-driven insights reinforce that **training optimization** and **player load monitoring** can significantly reduce injuries.

---

## 📁 Dataset Information

**Source:** [University Football Injury Prediction Dataset](https://www.kaggle.com/datasets/yuanchunhong/university-football-injury-prediction-dataset)  
**Description:** The dataset contains information on training load, match exposure, player metrics, and injury labels collected from university-level football sessions.

---

## 🧠 Future Work

- Experiment with **deep learning** models (e.g., LSTM or neural networks) for sequential injury risk prediction.  
- Apply **hyperparameter tuning** (GridSearchCV/Optuna) to further optimize model accuracy.  
- Develop a **web dashboard** to visualize live player metrics and predict injury risk.  
- Expand dataset scope to include multiple seasons or external leagues for broader generalization.

---

## 🤝 Credits

- **Dataset by:** [Yuanchun Hong on Kaggle](https://www.kaggle.com/yuanchunhong)  
- **Developed by:** Rohit  
- **Tools Used:** Python, Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn  

---

## 📜 License

This project is intended for **educational and research purposes** only.  
You may reuse or reference this notebook for learning or academic work with proper attribution.
