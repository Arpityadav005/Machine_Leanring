# HR Analytics – Employees Engagement

## 📌 Project Overview
This project explores the **HR Analytics – Employees Engagement** dataset to uncover key workforce insights, identify factors influencing employee engagement, and highlight patterns linked to retention and attrition.  
The analysis focuses on:
- Understanding workforce demographics and salary distribution.
- Exploring relationships between performance, engagement, and retention.
- Identifying trends to support HR decision-making.

---

## 📂 Dataset Information
The dataset includes information on:
- **Demographics**: Age, Gender, Marital Status.
- **Job-related**: Department, Position, Recruitment Source, Salary, Tenure.
- **Performance & Engagement**: Engagement Survey, Special Projects Count, Last Performance Review.
- **Retention Metrics**: Termination status, Reason for Termination, Absences.

---

## 🛠 Tools & Libraries Used
- **Python**: `pandas`, `numpy`
- **Visualization**: `matplotlib`, `seaborn`
- **Jupyter Notebook** for interactive analysis

---

## 📊 Analysis Steps

### 1. **Data Cleaning**
- Removed duplicate records.
- Handled missing values.
- Converted date columns to datetime format.
- Created new features:
  - **Age** (from Date of Birth)
  - **Tenure** (from Hire Date to current or termination date)
  - **Days since last performance review**

### 2. **Univariate Analysis**
- Distribution of salaries.
- Count of absences.
- Gender and marital status breakdown.
- Engagement survey scores.

### 3. **Bivariate Analysis**
- Salary vs Department.
- Marital Status vs Gender.
- Engagement survey vs Performance score.

### 4. **Multivariate Analysis**
- Relationship between Special Projects, Engagement Survey, and Performance.
- Impact of Absences on Performance and Engagement.

### 5. **Aggregated Insights**
- Termination rate by department and gender.
- Engagement score by recruitment source.
- Average salary and tenure per department.

---

## 🔍 Key Insights
- **High Volatility in Engagement**: Certain departments show large variations in engagement scores despite similar salary levels.
- **Attrition Trends**: Specific recruitment sources have higher turnover rates.
- **Tenure & Performance**: Employees with longer tenure tend to have higher engagement scores and better performance ratings.
- **Absences Impact**: Higher absences are often linked to lower performance scores.

---

## 📈 Future Improvements
- Build a **predictive model** to identify high-risk attrition cases.
- Create an **interactive HR Dashboard** in Power BI or Tableau.
- Perform **correlation analysis** and clustering for deeper segmentation.

---

## 📁 Repository Structure
