# Telco Customer Churn Prediction 📊

A Machine Learning project focused on predicting customer churn in a telecom company using classification algorithms such as Logistic Regression and Random Forest.

---

# 📌 Project Overview

Customer churn prediction helps telecom companies identify customers who are likely to discontinue their services. Predicting churn early allows companies to improve customer retention strategies and reduce revenue loss.

This project uses the IBM Telco Customer Churn dataset and applies:
- Data preprocessing
- Feature engineering
- Machine Learning models
- Cross-validation
- SHAP explainability

---

# 🎯 Objectives

- Predict whether a customer will churn or not
- Compare multiple ML algorithms
- Improve model accuracy while avoiding overfitting
- Evaluate models using multiple performance metrics
- Interpret model decisions using SHAP

---

# 🛠 Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- SHAP

---

# 📂 Dataset

Dataset Used:
- IBM Telco Customer Churn Dataset

Target Variable:
- `Churn`
  - Yes → Customer leaves company
  - No → Customer stays

---

# ⚙️ Models Implemented

## 1. Logistic Regression

Used as a baseline classification model.

### Why Logistic Regression?
- Simple and interpretable
- Performs well on binary classification
- Good benchmark model

---

## 2. Random Forest Classifier

Used for improved performance and feature importance analysis.

### Why Random Forest?
- Handles non-linear relationships
- Reduces overfitting using ensemble learning
- Provides better feature importance

---

# 🔄 Cross Validation Added

## What Was Added?
5-Fold Stratified Cross Validation was implemented.

### Why?
Instead of evaluating the model on only one train-test split, cross-validation:
- checks model stability
- reduces variance
- improves reliability of accuracy scores

### Benefits
- Better generalization
- More trustworthy performance metrics
- Reduced chance of overfitting

---

# 📈 Performance Metrics Used

The project evaluates models using:

- Accuracy Score
- F1-Score
- Confusion Matrix
- Classification Report
- ROC-AUC Score

---

# 🚀 Changes Made in Updated Version

The original notebook was improved with minimal code modifications.

---

## ✅ 1. Removed `customerID`

### Why?
`customerID` is unique for every customer and does not help prediction.

### Impact
- Reduced noise in model training
- Improved model learning

---

## ✅ 2. Added Proper Preprocessing

### Changes
- Converted `TotalCharges` to numeric
- Handled missing values
- Applied encoding
- Added scaling where required

### Impact
- Cleaner data
- Better model performance
- More stable predictions

---

## ✅ 3. Added Cross Validation

### Why?
To make evaluation more reliable.

### Impact
- Reduced overfitting
- Better estimate of real-world performance

---

## ✅ 4. Added F1-Score

### Why?
Accuracy alone is not reliable for imbalanced datasets like churn prediction.

### Impact
F1-score balances:
- Precision
- Recall

making evaluation more meaningful.

---

## ✅ 5. Tuned Random Forest Parameters

### Parameters Updated

```python
n_estimators = 300
max_depth = 10
min_samples_split = 5
min_samples_leaf = 2
```

### Why?
To improve generalization and avoid overfitting.

### Impact
- More stable predictions
- Better accuracy
- Improved F1-score

---

# 📊 Accuracy Improvement

| Model | Previous Accuracy | Updated Accuracy |
|---|---|---|
| Logistic Regression | ~78% | ~80.6% |
| Random Forest | ~76-78% | ~80.4% |

---

# 📈 Final Model Performance

## Logistic Regression
- Accuracy: ~80.6%
- F1 Score: ~0.60

## Random Forest
- Accuracy: ~80.4%
- F1 Score: ~0.59

These results fall within the ideal industry range for Telco Churn Prediction projects.

---

# 🧠 SHAP Explainability

SHAP was used to explain model predictions.

### Important Features Identified
- Contract type
- Tenure
- Internet service
- Monthly charges
- Online security
- Tech support

### Benefit
Helps understand:
- why customers churn
- which features influence predictions most

---

# 📌 Key Insights

- Customers with month-to-month contracts are more likely to churn
- Lower tenure customers churn more frequently
- Customers without online security and tech support have higher churn probability
- Fiber optic internet users showed higher churn tendency

---

# 📷 Example Output

The project includes:
- Confusion matrix
- Accuracy comparison
- SHAP summary plots
- Feature importance graphs

---

# ▶️ How to Run

## Install Dependencies

```bash
pip install pandas numpy scikit-learn matplotlib shap
```

## Run Notebook

```bash
jupyter notebook
```

Open:

```bash
customer_churn_updated.ipynb
```

---

# 📌 Future Improvements

Possible future enhancements:
- XGBoost implementation
- Hyperparameter tuning using GridSearchCV
- Deep Learning models
- Deployment using Flask/Streamlit
- Real-time churn prediction dashboard

---

# 👨‍💻 Conclusion

This project successfully predicts telecom customer churn using machine learning techniques while maintaining ideal accuracy and avoiding overfitting.

The updated version improved:
- model reliability
- evaluation quality
- interpretability
- overall performance

through preprocessing, cross-validation, and model tuning while keeping modifications to the original notebook minimal.
