# Mobile Price Classification - Project Overview and Approach

---

## 📂 Dataset  
Dataset source: [Mobile Price Classification - Kaggle](https://www.kaggle.com/datasets/iabhishekofficial/mobile-price-classification)  
- Training samples: 2000  
- Testing samples: Available (no `price_range` target)  
- Features: 20 input features describing mobile hardware and specifications  
- Target: `price_range` (4 classes indicating the price tier of the mobile phone)

---

## 🔍 Data Understanding  
- Dataset contains a mix of numerical and categorical features such as battery power, clock speed, presence of features like Bluetooth, dual SIM, four G, and screen characteristics.  
- Target variable is multiclass (0 to 3), representing price ranges.  
- No missing values detected and all columns are complete.  
- Explored basic statistics and unique value counts per feature to understand feature distributions and identify categorical vs continuous variables.

---

## ⚙️ Exploratory Data Analysis  
- Visualized target class balance through count plot showing equal distribution among 4 classes.  
- Analyzed feature distributions using boxplots, histograms, and pivot tables stratified by `price_range` to identify relationships between features and prices.  
- Identified important numeric features such as battery power, RAM, screen dimensions showing clear variation across price ranges.  
- Examined low-cardinality categorical features for their frequency and distribution by price range.

---

## 🧠 Modeling  
- Split data into train and test sets (80% train, 20% test).  
- Trained multiple classifiers including:
  - Decision Tree  
  - Logistic Regression  
  - Random Forest  
  - AdaBoost  
  - Bagging  
  - Voting Classifier (ensemble of Logistic Regression, Decision Tree, AdaBoost)  

- Visualized the Decision Tree to understand its decision rules.  
- Evaluated models using accuracy on the test set; Random Forest and Bagging showed the best results with accuracies around 86-87%, outperforming simpler models.

---

## 🔧 Hyperparameter Tuning  
- Performed grid search for:
  - Random Forest: tuned `n_estimators`, `max_depth`, and `oob_score`  
  - AdaBoost: tuned `n_estimators` and `learning_rate`  
  - Bagging: tuned `n_estimators` and `bootstrap`  
  - Decision Tree: tuned `criterion` and `max_depth`  
- Best parameters improved model accuracy, especially for Bagging showing ~87.5% accuracy after tuning.

---

## 📊 Results & Insights  
- Tuned Random Forest achieved overall best balance of complexity and performance.  
- Bagging ensemble performed slightly better after tuning, indicating robust performance gains from bootstrapped aggregations.  
- AdaBoost and Voting classifiers improved with tuning but lagged behind ensemble bagging methods.  
- Decision Tree model was prone to overfitting and benefited least from tuning.

---

## 🔮 Future Work  
- Explore stacking ensembles or boosting with other algorithms like XGBoost or LightGBM.  
- Apply feature selection or dimensionality reduction for speed improvements.  
- Implement cross-validation and utilize additional metrics like F1-score and confusion matrices for imbalanced classes or multiclass evaluation.  
- Experiment with neural networks or deep learning methods for potentially better performance.

---

## 📌 Usage  
- Compatible with Python 3 and scikit-learn.  
- Easily runnable in Kaggle Notebooks or any Jupyter environment with appropriate dependencies installed.

---
