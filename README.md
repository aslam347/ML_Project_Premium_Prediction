# 🏥 Healthcare Premium Prediction using Machine Learning

An end-to-end Machine Learning project that predicts **annual health insurance premium amounts** based on demographic, lifestyle, and medical attributes.

This project demonstrates a complete ML lifecycle from data preprocessing to deployment using Streamlit.

---

## 🚀 Project Overview

Insurance premium pricing depends on multiple risk-related factors such as age, BMI, smoking habits, medical history, and dependents.

This application uses Machine Learning models to estimate the **expected annual premium** for an individual.

---

## 🎯 Objective

To build a regression-based ML system that:

- Predicts annual insurance premium amount  
- Analyzes model performance and errors  
- Applies feature engineering using domain knowledge  
- Uses model segmentation to improve prediction accuracy  
- Deploys the solution as a web application  

---

## 📊 Dataset Features

| Feature | Description |
|---------|-------------|
| Age | Age of the individual |
| Gender | Male / Female |
| Region | Geographic region |
| Marital Status | Married / Unmarried |
| Number of Dependants | Number of family members covered |
| BMI Category | Underweight / Normal / Overweight / Obesity |
| Smoking Status | No Smoking / Occasional / Regular |
| Employment Status | Salaried / Self-Employed / Freelancer |
| Income Level | Income bracket |
| Income (Lakhs) | Numerical income value |
| Medical History | Existing diseases |
| Insurance Plan | Bronze / Silver / Gold |
| Annual Premium Amount | Target variable |

---

## 🧠 ML Workflow

### 1. Data Cleaning
- Handling missing values  
- Removing duplicates  

### 2. Exploratory Data Analysis (EDA)

### 3. Feature Engineering
- Health risk score derived from medical conditions  
- Normalization of risk score  

### 4. Encoding
- One-hot encoding for nominal variables  
- Ordinal encoding for insurance plan  

### 5. Model Training
- Linear Regression  
- Decision Tree Regressor  
- Random Forest Regressor  
- XGBoost Regressor  

### 6. Model Evaluation
- MSE  
- RMSE  
- R² Score  

### 7. Error Analysis
- Residual distribution  
- Segment-wise error comparison  

### 8. Model Segmentation
- Separate models for different age groups  

### 9. Deployment using Streamlit

---

## 🔬 Feature Engineering Highlight

A **Total Risk Score** was created using medical domain knowledge:

| Disease | Risk Score |
|---------|------------|
| Heart Disease | 8 |
| Diabetes | 6 |
| High Blood Pressure | 6 |
| Thyroid | 5 |
| No Disease | 0 |

This converts categorical medical history into a strong predictive numerical feature.

---

## 📈 Evaluation Metrics

| Metric | Purpose |
|--------|---------|
| MSE | Measures squared prediction error |
| RMSE | Average prediction error in premium units |
| R² Score | Percentage of variance explained |

---

## 🧩 Model Segmentation

Error analysis showed higher prediction errors among younger individuals.  
To improve accuracy:

- Separate models were trained for different age segments  
- Linear Regression performed well for younger group  
- Tree-based models performed better for others  

---

## 🌐 Web Application

Built with **Streamlit** to allow users to input personal and health information and receive predicted annual premium.

---

## 🛠 Tech Stack

- Python  
- Pandas  
- NumPy  
- Scikit-Learn  
- XGBoost  
- Streamlit  
- Joblib  

---

## 📁 Project Structure

```
ML_Project_Premium_Prediction/
│
├── app/
│   └── main.py
│
├── artifacts/
│   ├── model_young.joblib
│   ├── model_rest.joblib
│   ├── scaler_young.joblib
│   ├── scaler_rest.joblib
│
├── notebook/
│
├── requirements.txt
└── README.md
```

---

## ⚙️ Installation & Run

```bash
git clone <repo_link>
cd ML_Project_Premium_Prediction
pip install -r requirements.txt
streamlit run app/main.py
```

---

## 📜 Requirements

```
joblib==1.5.3
pandas==2.0.2
streamlit==1.35.0
numpy==1.26.4
scikit-learn==1.7.2
xgboost==3.1.3
```

---

## 💡 Key Learnings

- Regression modeling  
- Feature engineering using domain knowledge  
- Error analysis techniques  
- Model segmentation  
- ML deployment  

---

## 👨‍💻 Author

**Mohamed Aslam M**  
Machine Learning & AI Enthusiast
