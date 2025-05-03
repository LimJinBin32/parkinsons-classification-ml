# Classification of parkinson's disease using decision tree and Ensemble method.
---

## 🎯 Project Objective

To develop and compare two machine learning models:
- A **Decision Tree Classifier**
- An **Ensemble Method Classifier** (Random Forest)

The models were evaluated on accuracy, precision, recall, and other classification metrics using the provided `parkinson_disease_assignment.csv` dataset.

---

## 🧪 Dataset Summary

- **Source**: Provided and modified by the lecturer (includes a new column, randomized rows, and missing values)
- **Target Variable**: `Status` (1 = Parkinson’s, 0 = Healthy)
- **Features**: Voice frequency measures, jitter, shimmer, HNR, etc
- **Class Distribution**: Highly imbalanced (~75% Parkinson’s)
- **Preprocessing Steps**:
  - Removed nulls and duplicates
  - Dropped irrelevant columns
  - Label encoded the target variable
  - Used **stratified train-test split** (80/20) to preserve class distribution

---

## ⚙️ Models Implemented

### 1. Decision Tree Classifier
- Built using `sklearn.tree.DecisionTreeClassifier`
- Hyperparameters tuned via GridSearchCV: `max_depth`, `min_samples_split`, `min_samples_leaf`, `max_features`


### 2. Random Forest Classifier (Ensemble Method)
- Built using `sklearn.ensemble.RandomForestClassifier`
- Applied bagging techniques with multiple decision trees

---

## 📊 Model Comparison

| Metric             | Decision Tree  | Random Forest            |
|--------------------|----------------|--------------------------|
| Accuracy (Test)    | 92.1%          | 87.0%                    |
| AUC Score (Test)   | 0.92           | 0.72                     |
| Recall (Minority)  | Higher         | Lower                    |
| Train Time         | Faster         | Slower (~2 mins longer)  |


## 📈 Evaluation techniques

Both models were evaluated using:
- Accuracy
- Precision, Recall, F1 Score
- Confusion Matrix
- ROC Curve and AUC Score

---

## 🧰 Tools & Technologies

- Python (Google Colab)
- Pandas, NumPy
- Scikit-learn
- Matplotlib, Seaborn

---

⚠️ Notes

The dataset is **not included** due to academic licensing restrictions.

---

🙋‍♂️ Author

Lim Jin Bin
Y2 AI & Data Engineering
Nanyang Polytechnic
Module: Machine Learning

