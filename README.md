# Customer Churn Prediction using Machine Learning

## 📌 Overview
Customer churn prediction is a common real-world machine learning problem where the goal is to identify customers who are likely to leave a service. Retaining existing customers is often more cost-effective than acquiring new ones, making churn prediction highly valuable for businesses such as telecom companies, SaaS platforms, and subscription-based services.

In this project, a machine learning model is built to predict whether a customer will **churn (Yes)** or **stay (No)** based on customer demographics, service usage, contract details, and billing information.

---

## 🎯 Problem Statement
To build a machine learning model that predicts customer churn using historical customer data and to evaluate the model using appropriate metrics suitable for imbalanced classification problems.

---

## 📊 Dataset Information
- **Dataset Name:** Telco Customer Churn Dataset  
- **Source:** Kaggle  
- **Target Variable:** `Churn` (Yes / No)

### Dataset Features Include:
- Customer demographics (gender, senior citizen, dependents)
- Subscription details (tenure, contract type)
- Services used (internet, streaming, tech support, etc.)
- Billing information (monthly charges, total charges, payment method)

---

## 🧠 Learning Approach & Concepts Covered

This project was designed to strengthen **machine learning fundamentals** while following **industry-standard practices**.

### Concepts Applied:
- Supervised Learning (Classification)
- Binary Classification
- Data Cleaning & Handling Missing Values
- Feature Engineering
- Pipelines and ColumnTransformer
- Preventing Data Leakage
- Model Evaluation with appropriate metrics
- Cross-Validation
- Model Comparison

---

## ⚙️ Data Preprocessing

Real-world datasets are rarely clean. The following preprocessing steps were applied:

### 1. Handling Hidden Missing Values
- The `TotalCharges` column contained empty strings instead of valid numeric values.
- These were safely converted to `NaN` using:
  ```python
  pd.to_numeric(errors='coerce')
## ⚙️ Data Preprocessing

### 2. Feature Separation
- Features (`X`) and target (`y`) were separated to avoid **data leakage**.

### 3. Numerical Feature Processing
- Missing values were imputed using **median**
- Features were scaled using **StandardScaler**

### 4. Categorical Feature Processing
- Missing values were imputed using the **most frequent category**
- Categorical variables were converted to numerical format using **One-Hot Encoding**
- `handle_unknown='ignore'` was used to ensure robustness on unseen categories

### 5. Pipeline-Based Preprocessing
All preprocessing steps were handled inside a **scikit-learn Pipeline** combined with a **ColumnTransformer** to:
- Ensure consistency
- Prevent data leakage
- Enable clean cross-validation and model comparison

---

## 🤖 Models Used

### 1️⃣ Logistic Regression (Baseline Model)
- Used as an interpretable baseline model
- Helped establish a reference performance

### 2️⃣ Random Forest Classifier (Final Model)
- Captured non-linear relationships in the data
- Handled class imbalance using `class_weight='balanced'`
- Achieved better overall performance compared to the baseline

---

## 📏 Evaluation Metrics

Since customer churn data is **imbalanced**, accuracy alone can be misleading.  
Therefore, the following metrics were used:

- **Precision**
- **Recall**
- **F1 Score** (primary metric)
- **Confusion Matrix**
- **Cross-Validation (5-Fold)**

### Why F1 Score?
F1-score provides a balance between precision and recall, making it suitable for imbalanced classification problems where both false positives and false negatives are important.

---

## 📈 Results

### Random Forest Performance
- **Test F1 Score:** `0.57`
- **Average Cross-Validation F1 Score (5-fold):** `0.60`

The close alignment between test and cross-validation scores indicates good model generalization and minimal overfitting.

---

## 🏁 Conclusion

The Random Forest model outperformed Logistic Regression and demonstrated stable performance across cross-validation. Due to its ability to capture non-linear patterns and handle class imbalance effectively, Random Forest was selected as the final model for customer churn prediction.

This project demonstrates a complete, end-to-end machine learning workflow following best practices used in real-world industry applications.

---

## 🚀 Future Improvements
- Hyperparameter tuning using GridSearchCV
- Threshold optimization to improve recall for churned customers
- Feature importance analysis
- Deployment as a web application or API

---

## 🛠️ Technologies Used
- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn

---

## 📌 Author
**Archit Bankey**
