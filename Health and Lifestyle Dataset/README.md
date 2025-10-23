# Health and Lifestyle Dataset - Disease Risk Classification

---

## 📂 Dataset  
Dataset used: [Health and Lifestyle Dataset - Kaggle](https://www.kaggle.com/datasets/chik0di/health-and-lifestyle-dataset)  
- Total samples: 100,000  
- Features: 16 (15 predictive + 1 target)  
- Target: `disease_risk` (binary classification: 0 = low risk, 1 = high risk)

---

## 🔍 Data Overview  
- Mix of numerical features (age, bmi, daily_steps, sleep_hours, blood pressure, cholesterol, etc.) and categorical gender feature.  
- No missing values in the dataset - clean and ready for analysis.  
- Observed class imbalance: ~75% samples in class 0 and ~25% in class 1.

---

## ⚙️ Data Exploration & Feature Understanding  
- Described basic statistics for numerical features including mean, median, min, max, standard deviation.  
- Explored value counts and distributions for categorical variables like gender, smoker status, alcohol use, and family history.  
- Visualized class distribution using count and pie charts for disease risk variable.  
- Used histograms, KDE plots, and boxplots to illustrate feature distributions and detect outliers.  
- Analyzed feature distributions separately for disease risk classes to identify potential discriminative patterns.

---

## 🧩 Feature Engineering  
- Encoded `gender` into numeric values (Male=1, Female=0) for model compatibility.  
- Removed `id` column as it is an identifier and not predictive.  
- Examined correlation matrix and visualized it via heatmap to identify strongly correlated features with the target.  
- Selected significant features based on correlation and domain knowledge for model input.

---

## 🧠 Modeling Approach  
- Split data into training and testing subsets (80-20 split).  
- Tested multiple classification models:
  - Logistic Regression  
  - K-Nearest Neighbors  
  - Support Vector Machine  
  - Decision Tree  
  - Random Forest  
  - Gradient Boosting  
  - AdaBoost  
  - Bagging Classifier  
- Evaluated models using accuracy, F1-score, precision, recall, and confusion matrices.  

---

## 📊 Results  
- Logistic Regression and SVM showed decent training but failed to predict positive cases resulting in 0 F1-score.  
- K-Nearest Neighbors and Bagging showed moderate capability to detect positive class.  
- Random Forest and Gradient Boosting models near 75% accuracy but poor minority class detection, indicated by low F1-scores.  
- Overall, models struggled due to class imbalance and possibly feature complexity.

---

## 🛠️ Deep Learning Model  
- Built a feedforward neural network with multiple dense layers (200, 128, 100, 50 units) and ReLU activations.  
- Output layer used sigmoid activation for binary classification.  
- Compiled with Adam optimizer and binary cross-entropy loss.  
- Trained for 10 epochs using batch size of 32 and 20% validation split.  
- Achieved ~75% accuracy on test data with stable training and validation curves.

---

## 🔮 Conclusion and Next Steps  
- The dataset is well-structured and clean, but imbalance in classes poses challenges for model performance, especially minority class detection.  
- Further improvements can be made through:
  - Advanced sampling methods (SMOTE, undersampling) to handle imbalance,  
  - Hyperparameter tuning,  
  - Feature transformation and selection,  
  - Using more complex models or ensembles,  
  - Incorporating cross-validation and more robust metrics like ROC-AUC.

---

## 📌 Notes  
- This project showcases best practices in exploratory data analysis (EDA), feature engineering, classical ML, and a baseline deep learning model for disease risk prediction.  
- It provides the foundation for further development and deployment of healthcare risk classification systems.

---
