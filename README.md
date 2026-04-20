# 🧠 Heart Stroke Prediction — Risk Modeling & Analysis

This project focuses on predicting the likelihood of stroke using patient demographics and health indicators. It combines **statistical analysis and machine learning** to identify key risk factors and build interpretable predictive models.

---

## 📊 Problem Statement

Stroke is a leading cause of mortality and long-term disability.  
Early identification of high-risk individuals can significantly improve preventive care.

This project aims to:
- Identify key health factors contributing to stroke risk  
- Build predictive models for early detection  
- Provide interpretable insights for healthcare decision-making  

---

## ⚙️ Tech Stack

**Language:** R  
**Data Processing:** dplyr, plyr  
**Visualization:** ggplot2, cowplot  
**Statistical Analysis:** gmodels, regclass  
**Machine Learning:** caret, glmnet, pROC, Metrics  

---

## 🧼 Data Preprocessing

To ensure data quality and model reliability:

- Removed inconsistent category (`gender = "Other"`)  
- Converted categorical variables:
  - `stroke`, `hypertension`, `heart_disease` → factors  
- Cleaned BMI column:
  - Converted to numeric  
  - Removed missing values (NA rows)  

---

## 📈 Exploratory Data Analysis (EDA)

Performed analysis to understand relationships between features and stroke:

- Distribution analysis of:
  - Age  
  - Average Glucose Level  
  - BMI  
- Visualizations:
  - Histograms  
  - Boxplots (stroke vs non-stroke comparison)

👉 Key insight: Stroke likelihood increases significantly with age and health conditions.

---

## 📊 Hypothesis Testing

### 1. T-Test (BMI)
- Tested whether BMI differs significantly between stroke and non-stroke patients  

### 2. Chi-Square Test
- Checked independence between:
  - Residence Type vs Stroke occurrence  

👉 Provided statistical validation of feature importance.

---

## 🧠 Predictive Modeling

### 1. Logistic Regression

- Built baseline model using all features  
- Refined to a **pruned model** using key predictors:
  - Age  
  - Hypertension  
  - Average Glucose Level  

---

### 2. Lasso Regression (Regularization)

- Applied **L1 regularization** using `glmnet`  
- Used **10-fold cross-validation** to select optimal λ (lambda)  
- Reduced overfitting and selected most impactful features  

---

## 🏆 Key Results & Insights

Final Logistic Regression Model:

- **Age**  
  → Each unit increase increases stroke odds by **~7%**

- **Hypertension**  
  → Increases stroke risk by **~67%**

- **Heart Disease**  
  → Increases stroke risk by **~48%**

---

## 📉 Model Evaluation

- Evaluated using **ROC Curve**  
- Measured performance using **AUC (Area Under Curve)**  

👉 Ensured model reliability and predictive capability.

---

## 📂 Repository Structure
```bash
Heart-Stroke-Prediction/
├── Heart_Stroke_Analysis_Code.R
├── healthcare-dataset-stroke-data.csv
├── Heart_Stroke_Analysis_Presentation.pptx
├── Heart_Stroke_Analysis.docx


---

## 🧠 Key Takeaways

- Age, hypertension, and heart disease are strong predictors of stroke  
- Regularization (Lasso) improves model robustness  
- Statistical + ML combination provides both **interpretability and prediction power**

---

## 🚀 Future Improvements

- Add more advanced models (Random Forest, XGBoost)  
- Handle class imbalance (SMOTE / resampling techniques)  
- Deploy as a real-time prediction API  
- Integrate with healthcare dashboards  

---

## 🎯 Final Thought

This project demonstrates how **data analysis + machine learning** can be used to uncover meaningful health insights and support early intervention strategies.
