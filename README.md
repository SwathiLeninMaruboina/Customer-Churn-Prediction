# 📉 Customer Churn Prediction | End-to-End ML Project

## 🚀 Project Overview
Customer churn occurs when customers stop using a company’s services. Since acquiring new customers is significantly more expensive than retaining existing ones, churn prediction is a critical business problem.  

This project builds a machine learning pipeline to predict customer churn using telecom subscription data and provides actionable business insights.

---

## 🎯 Business Objective
- Predict whether a customer will churn (Yes/No)  
- Identify high-risk customers early  
- Enable proactive retention strategies  
- Reduce revenue loss  

---

## 📌 Business Success Metric
- Capture ≥ 65% of churners by targeting the top 25% highest-risk customers  
- **Recall prioritized over accuracy** because missing a churner = lost revenue

---

## 📊 Dataset Information
- **Number of customers:** 7,043  
- **Features:** 21  
- **Target variable:** `Churn`  
- **Churn rate:** 26.5%  

**Feature Categories:**  
- **Demographics:** Gender, SeniorCitizen  
- **Services:** InternetService, StreamingTV, TechSupport  
- **Account:** Contract, Tenure  
- **Billing:** MonthlyCharges, TotalCharges  

---

## 🧠 Machine Learning Approach

### 1️⃣ Data Preprocessing
- Converted `TotalCharges` to numeric  
- Handled missing values  
- Label encoding for categorical variables  
- Feature scaling using `StandardScaler`  
- Engineered new features:  
  - `AvgMonthlySpend`  
  - `Is_Long_Term_Contract`  
  - `High_Monthly_Charges`  

### 2️⃣ Models Trained

| Model                  | Recall | F1 Score | ROC-AUC |
|------------------------|--------|----------|---------|
| Logistic Regression    | 0.78   | 0.61     | 0.85    |
| Random Forest          | 0.69   | 0.62     | 0.84    |
| XGBoost                | 0.77   | 0.63     | 0.83    |

**🏆 Final Selected Model: Tuned Random Forest**  
- After threshold tuning:  
  - Recall: 0.84  
  - ROC-AUC: 0.84  
- Successfully captures majority of churners

---

## 🔍 Key Insights from EDA
- Short-tenure customers churn more  
- Higher monthly charges increase churn risk  
- Month-to-month contracts have highest churn  
- Churn dataset is moderately imbalanced  

---

## 📈 Model Evaluation
- 5-fold cross-validation performed  
- ROC curve comparison  
- Threshold optimization for recall  
- Feature importance analysis  

---

## 🔝 Most Important Features
- Contract Type  
- Tenure  
- Online Security  
- Tech Support  
- Monthly Charges  
- Total Charges  
- Internet Service  
- Avg Monthly Spend  

---

## 📂 Project Structure
---

├── README.md
├── customer_churn.csv
├── churn_prediction.ipynb
├── model.pkl
└── requirements.txt

---

## ⚙️ Tech Stack
- Python  
- Pandas  
- NumPy  
- Scikit-learn  
- XGBoost  
- Matplotlib  
- Seaborn  

---

## 💼 Business Impact
This model enables:  
- Targeted marketing campaigns  
- Reduced customer acquisition cost  
- Higher customer lifetime value  
- Data-driven retention strategies  

---

## 🔮 Future Improvements
- Use SMOTE for imbalance handling  
- Deploy model using Flask or FastAPI  
- Add SHAP explainability  
- Hyperparameter tuning with GridSearchCV  
- Deploy as Streamlit dashboard  

---
