 Chronic Kidney Disease (CKD) – Exploratory Data Analysis
⚠️ PROBLEM: CHRONIC KIDNEY DISEASE
Chronic Kidney Disease (CKD) is a serious health issue where kidney function declines over time.

Early detection is crucial to prevent complete kidney failure.

Medical datasets often contain missing values, inconsistent entries, and mixed data types.

Without proper cleaning and analysis, models built on such data can be unreliable.

🎯 PROJECT GOAL
Clean, explore, and visualize the CKD dataset

Identify patterns between clinical features and CKD diagnosis

Prepare a clean dataset for future predictive modeling

📂 DATASET INFORMATION
File: kidney_disease.csv

Rows: 400

Columns: 26 (patient demographics, lab results, medical history, target variable)

Target Variable: class (1 = CKD, 0 = Not CKD)

🧰 LIBRARIES USED
Library	Purpose
pandas, numpy	Data cleaning & manipulation
matplotlib, seaborn	Data visualization
plotly.express	Interactive plots
scikit-learn	Data preprocessing

📉 MAJOR DATA ISSUES FOUND
Missing Values → Several lab results were missing for many patients

Inconsistent Categorical Labels → e.g., " yes", "\tno" instead of "yes"/"no"

Mixed Data Types → Numeric values stored as strings

Irrelevant Columns → Patient id column not useful for analysis

✅ CLEANING STEPS TAKEN
Dropped Irrelevant Columns – Removed patient ID

Renamed Columns – Made them consistent and readable

Fixed Categorical Inconsistencies – Standardized yes/no responses

Converted Data Types – Turned numeric strings into actual numbers

Mapped Target Variable – ckd → 1, notckd → 0

🔍 EDA HIGHLIGHTS
📊 Univariate Analysis
Age distribution shows most patients are 40–70 years old

CKD patients often have higher serum creatinine & blood urea

Hypertension and diabetes are frequent among CKD patients

🔗 Bivariate Analysis
Hypertension ↔ CKD → Strong positive relationship

Older age → Higher blood pressure trend

Diabetes + Hypertension → High CKD risk group

📈 VISUAL INSIGHTS
Age Distribution

Hypertension Count

Albumin Levels by Diabetes Status

🔄 NEXT STEPS
Feature Engineering – Create new features from existing lab results

Class Imbalance Handling – Apply SMOTE or upsampling if needed

Model Building – Train ML model for CKD prediction

📌 WHY THIS PROJECT MATTERS
By performing structured EDA, we ensure:

Cleaner data → better ML performance

Early detection insights → supports healthcare decision-making

Reproducible process → can be applied to similar medical datasets

