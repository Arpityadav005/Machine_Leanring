✈️ Travel Data Analysis (EDA)
Exploring customer travel patterns, demographics, and product adoption trends.
A deep dive into insights from the Travel.csv dataset.

📌 Table of Contents
Project Overview

Dataset Details

EDA Workflow

Key Insights

Visualizations

Tech Stack

How to Run

Results & Next Steps

📝 Project Overview
This project performs Exploratory Data Analysis on the Travel dataset to:

Understand customer demographics and travel preferences

Identify factors influencing product adoption (ProdTaken)

Explore relationships between travel duration, income, and satisfaction scores

Prepare data for predictive modeling

📂 Dataset Details
Feature	Description
Age	Age of the customer
TypeofContact	Method of first contact (e.g., Company Invited, Self Inquiry)
CityTier	Customer’s city classification
DurationOfPitch	Duration (minutes) of the sales pitch
Occupation	Customer’s occupation
Gender	Gender of the customer
NumberOfPersonVisiting	Total people visiting
NumberOfFollowups	Number of follow-ups before booking
ProductPitched	Product suggested to the customer
PreferredPropertyStar	Star rating of preferred property
MaritalStatus	Customer’s marital status
Passport	Whether the customer has a passport (1 = Yes, 0 = No)
MonthlyIncome	Monthly income of the customer
Designation	Professional designation
PitchSatisfactionScore	Sales pitch satisfaction rating
OwnCar	Whether the customer owns a car
ProdTaken	Whether the customer took the product (1 = Yes, 0 = No)

📁 Source: Provided Travel.csv dataset

🛠 EDA Workflow
<details> <summary>Click to expand full workflow</summary>
Data Cleaning

Standardized inconsistent text entries (e.g., "Fe Male" → "Female")

Converted integer-coded categories (Passport, OwnCar, CityTier) to categorical type

Removed rows with missing values

Univariate Analysis

Countplots for categorical features

Histograms & KDE plots for numerical features

Bivariate Analysis

Scatter plots for numeric-numeric relationships

Stacked bar charts for category-category comparisons

Bar plots & line plots for numeric-category relationships

Multivariate Analysis

Violin plots for category vs. numeric distribution

3D scatter plots for Age, Monthly Income, and Duration of Pitch

Correlation heatmap for numeric variables

Feature Engineering Prep

Dataset ready for encoding & scaling

Identified potential new features (e.g., income per person)

</details>
📈 Key Insights
✅ Most customers fall in the 30–40 age group
✅ Higher Pitch Satisfaction Score correlates with increased product adoption
✅ Customers with passports have a higher booking rate
✅ Income distribution skews towards middle-income earners
✅ Certain occupations (e.g., Salaried) have higher travel interest

🖼 Visualizations
Age Distribution	Product Adoption by Marital Status

🛠 Tech Stack
Python (pandas, numpy, matplotlib, seaborn)

Jupyter Notebook

Plotly for interactive plots

