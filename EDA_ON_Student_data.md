📊 Student Performance & Outlier Analysis (UCI Student “por” dataset)

Analyze student demographics, study habits, alcohol consumption, and grades to uncover patterns that influence performance and to detect & handle outliers robustly.

🎯 Problem Statement

Understand which factors (age, study time, internet access, family context, etc.) relate to final grade G3.

Detect outliers (e.g., in absences, G1–G3, studytime) using IQR and decide whether to keep, cap, or remove them.

Provide a clean, reproducible EDA workflow (univariate, bivariate, multivariate) with actionable insights.

✅ What This Project Solves

Data quality checks: missing values, duplicates, dtypes, shape.

Distribution understanding: age, address (Urban/Rural), alcohol consumption (Dalc, Walc), activities, etc.

Imbalance checks: school (GP vs MS), gender.

Outlier detection with IQR across numeric features.

Correlation analysis (heatmap) for G1, G2, G3, studytime, absences, etc.

Clean train/test split with a correct feature/target definition (no indexing mistakes).

🧠 Concepts Covered (Topics Included)

EDA: Univariate, Bivariate, Multivariate

Value counts, proportions, group-wise comparisons

Boxplots / distributions for outlier spotting

Correlation heatmap (numeric-only)

IQR-based outlier detection (Q1 − 1.5·IQR, Q3 + 1.5·IQR)

Train/test split and feature/target selection best practices

(Optional) Encoding strategy if modeling later (One-Hot for categoricals)

📂 Dataset (what you used)

File: student-por.csv

Rows: 649, Columns: 33

Categorical (examples): school, sex, address, famsize, Pstatus, Mjob, Fjob, reason, guardian, schoolsup, famsup, paid, activities, nursery, higher, internet, romantic

Numeric (examples): age, traveltime, studytime, failures, famrel, freetime, goout, Dalc, Walc, health, absences, G1, G2, G3

From your EDA:

~65% students from GP; ~35% from MS

~70% Urban (U); ~30% Rural (R)

Walc skewed toward low consumption; studytime shows positive relation with G3 (barplot)

Mothers show slightly higher education distribution vs fathers

Outliers present in absences, G1–G3, studytime, etc.

🛠 Libraries

Core: pandas, numpy

Plots: matplotlib, seaborn

ML utilities: scikit-learn (for train_test_split)








student-grades-analysis/
├─ data/
│  └─ student-por.csv
├─ notebooks/
│  └─ 01_eda_outliers.ipynb
├─ scripts/
│  ├─ eda.py
│  └─ outliers.py
├─ results/
│  ├─ figures/
│  └─ tables/
├─ README.md
└─ requirements.txt
