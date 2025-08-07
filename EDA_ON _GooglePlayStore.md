# 📱 Google Play Store Data Analysis - EDA Project

This repository contains an exploratory data analysis (EDA) project using the **Google Play Store dataset**. The objective is to clean, profile, and analyze the data to uncover patterns in app ratings, sizes, reviews, and more.

---

## 📁 Dataset

- **Source**: [Kaggle - Google Play Store Apps](https://www.kaggle.com/datasets/lava18/google-play-store-apps)
- **Format**: CSV
- **Rows**: 10,841
- **Columns**: 13

---

## 🎯 Objectives

- Understand app characteristics such as category, size, rating, and price.
- Clean inconsistent and missing data.
- Perform descriptive and statistical EDA.
- Prepare the dataset for future visualization and machine learning.

---

## 📊 EDA Workflow

### 1. 📥 Data Loading
- Loaded `googleplaystore.csv` using `pandas`.

### 2. 🧹 Initial Exploration
- Viewed dataset shape, head, tail, random samples.
- Displayed column names and data types.
- Checked for duplicates and dropped them.
- Examined missing values and invalid entries.

### 3. 🧪 Data Profiling
- Used `.info()`, `.describe()`, and `.describe(include='all')` to summarize data.
- Profiled key numeric and categorical columns:
  - `Rating`
  - `Reviews`
  - `Size`
  - `Installs`
  - `Type`
  - `Price`

### 4. 🔧 Data Cleaning

#### ✔️ Converted `Reviews` to Integer
- Removed one invalid non-numeric entry at index 9990.
- Cast `Reviews` column to `int`.

#### ✔️ Cleaned and Converted `Size` to Numeric (in KB)
- Used a custom function to:
  - Convert values like `"19M"` to `19456` KB
  - Convert `"14k"` to `14`
  - Replace `"Varies with device"` with `NaN`

---

## ✅ Current Dataset Status

| Description           | Value           |
|-----------------------|-----------------|
| Rows (after cleaning) | 10,358          |
| Columns               | 13              |
| Duplicates Removed    | 483             |
| Reviews Type          | Integer         |
| Size Converted        | KB (float)      |

---

## 📌 Technologies Used

- **Python**
- **Jupyter Notebook**
- **Libraries**:
  - `pandas`
  - `numpy`
  - `matplotlib` (to be used later)
  - `seaborn` (to be used later)

---

## 🧠 Next Steps

- Analyze and clean other columns (`Installs`, `Price`, `Rating`).
- Visual EDA using Seaborn and Matplotlib.
- Correlation heatmaps and feature relationships.
- Outlier detection and treatment.
- Build machine learning-ready dataset.

---

## 🧾 License

This project is for educational purposes only. Dataset sourced from Kaggle.

---

## 👨‍💻 Author

**Arpit Yadav**  
Aspiring Data Scientist | Data Analyst  
🔗 [LinkedIn](https://www.linkedin.com/in/arpit-yadav2004/)  
📌 [Portfolio](#) (add later if available)

