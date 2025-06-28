# Employee Retention Prediction

This repository presents a logistic regression-based predictive model that estimates the likelihood of employee attrition based on a variety of features including job satisfaction, overtime, tenure, and company-level metrics. The project includes in-depth EDA, model building, feature selection, and performance evaluation.

---

## Objective

To analyze employee data and predict the probability of employee attrition using a statistical model that is both accurate and interpretable. The solution supports HR in identifying at-risk employees and making informed retention decisions.

---

## Dataset Overview

- **Rows:** 74,610  
- **Columns:** 24  
- **Target Variable:** `Attrition` (Yes/No)

**Key Features:**
- **Demographics:** Age, Gender, Marital Status, Education
- **Job Details:** Role, Satisfaction, Performance Rating, Overtime
- **Company Factors:** Remote Work, Recognition, Work-Life Balance
- **Tenure:** Company tenure, Years in Current Role, Promotions

---

## Exploratory Data Analysis (EDA)

### ✅ Univariate Analysis:
- Most employees are aged between 30 and 40.
- High concentration of employees with ≤2 promotions.
- Majority monthly income is under 20,000.

### ✅ Bivariate Analysis:
- **Gender:** Males show lower attrition.
- **Overtime:** Strongly linked to higher attrition.
- **Work-Life Balance:** Poor balance → higher risk of leaving.
- **Recognition:** Lack of appreciation contributes to exits.
- **Remote Work:** Onsite employees are more likely to leave.

---

## Data Cleaning & Feature Engineering

- Missing values in features like `DistanceFromHome` and `CompanyTenure` were imputed using median strategy.
- Dropped `Employee_ID` as it had no predictive value.
- Created dummy variables for categorical features.
- Numerical features were scaled before model training.

---

## Model Building: Logistic Regression

- **Feature Selection:** Recursive Feature Elimination (RFE)
- **15 Best Features** selected for final model
- Checked for:
  - p-values < 0.05
  - VIF < 5 (no multicollinearity)

### ✅ Training Metrics:
- **Accuracy:** 73.9%
- **Recall:** 75.8%
- **Precision:** 75.0%
- **Specificity:** 71.8%
- **AUC Score:** 0.825

### ✅ Validation Metrics:
- **Accuracy:** 73.7%
- **Recall:** 75.9%
- **Precision:** 74.2%
- **Specificity:** 71.4%

No signs of overfitting. The model generalizes well.

---

## 🗝Key Business Insights

- **Top Attrition Drivers:**
  - Overtime
  - Lack of recognition
  - Absence of remote work options
  - Low job satisfaction
  - Single marital status
  - Poor work-life balance

- **HR Recommendations:**
  - Offer remote work flexibility
  - Introduce structured recognition programs
  - Improve work-life balance initiatives

---
 
## Steps To Use
### 1. Clone the repository
```bash
git clone https://github.com/tiyasa94/employee-retention-prediction.git
cd employee-retention-prediction
```

### 2. Install dependencies
```bash
pip install -r requirements.txt
```

### 3. Launch the notebook
```bash
Predicting_Employee_Retention_Starter.ipynb
```

---

## Output
Final model with optimal cutoff for predicting attrition

Interpretable coefficients for HR understanding

Classification reports and ROC-AUC for evaluation


---

## Author
Tiyasa Mukherjee
AI Engineer | Data Scientist | Generative AI & NLP Enthusiast
