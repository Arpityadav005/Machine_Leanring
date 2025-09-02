# Flight Price Prediction – EDA & Feature Engineering

Welcome to the Exploratory Data Analysis (EDA) journey for the Flight Price dataset!  
This README is designed to be interactive and beginner-friendly, so you can follow step by step and understand why we do each transformation. 🚀

---

## 📌 Dataset Overview

We’re working with the **flight_price.xlsx** dataset.  
It contains **10,683 rows × 11 columns** with information like airlines, source, destination, departure/arrival times, duration, total stops, and price.

### Sample of the dataset:

| Airline    | Date_of_Journey | Source    | Destination | Route                     | Dep_Time | Arrival_Time   | Duration | Total_Stops | Additional_Info | Price |
|------------|-----------------|-----------|-------------|---------------------------|----------|----------------|----------|-------------|-----------------|-------|
| IndiGo     | 24/03/2019      | Banglore  | New Delhi   | BLR → DEL                 | 22:20    | 01:10 22 Mar   | 2h 50m   | non-stop    | No info         | 3897  |
| Air India  | 1/05/2019       | Kolkata   | Banglore    | CCU → IXR → BBI → BLR     | 05:50    | 13:15          | 7h 25m   | 2 stops     | No info         | 7662  |

---

## 🔎 Step 1: Data Cleaning

- **Check shape & info**  
  Rows: 10,683  
  Columns: 11  
- Most features are of **object type**.  
- **Handle Missing Values**  
  Route and Total_Stops had 1 missing value each → **dropped the row**.  
- ✅ Now the dataset has **10,682 rows**.

---

## 📅 Step 2: Feature Engineering on Date

The `Date_of_Journey` column is in string format (`24/03/2019`).  
We split it into **Day, Month, Year** for better analysis.


- ✅ Now we can analyze **seasonal trends** and price variations across months.

---

## 🕒 Step 3: Time Features

- **Arrival Time**  
  Extracted hour and minutes from `Arrival_Time`.  
  Removed the extra date part (e.g. `01:10 22 Mar` → `01:10`).

- **Departure Time**  
  Extracted `Dep_hour` and `Dep_mins` from `Dep_Time`.

👉 **Why?** Because departure/arrival hours strongly influence ticket prices.

---

## 🛑 Step 4: Stops (Categorical → Numeric)

The `Total_Stops` column had values like:

- non-stop → 0  
- 1 stop → 1  
- 2 stops → 2  
- 3 stops → 3  
- 4 stops → 4  

- ✅ Converted to **numeric format** for ML models.

---

## 🗺️ Step 5: Route Column

- `Route` was redundant (already captured by `Source`, `Destination`, and `Total_Stops`).  
- 🗑️ **Dropped it to avoid multicollinearity**.

---

## ⏱️ Step 6: Duration Feature

- `Duration` column was messy (examples: `2h 50m`, `19h`, `5m`, etc.).  
- Split into:  
  - `duration_hour`  
  - `duration_mins`  
- Converted both into **integers** for better numerical handling.

---

## 📋 Step 7: Additional Info

- Mostly contained `"No info"` (over 80% of rows).  
- Decided to keep it for encoding, since some values like `"Business class"`, `"No check-in baggage"` may add insight.

---

## 🏷️ Step 8: Encoding Categorical Features

Used **OneHotEncoding** on:

- `Airline`  
- `Source`  
- `Destination`  
- `Additional_Info`  

This expanded the dataset to **44 columns**.

### Example encoded features:

- `Airline_IndiGo`  
- `Airline_Air India`  
- `Source_Delhi`  
- `Destination_Cochin`  
- `Additional_Info_No info`

---

## ✅ Final Dataset

- Rows: **10,682**  
- Columns: **44**  
- Mix of numerical features (`stops`, `day`, `time`, `duration`, `price`) and one-hot encoded features (`airline`, `source`, `destination`).

This final dataset is now **cleaned, structured, and ready for modeling** 🎯

---

## 💡 Key Learnings

- Dates must be split into **Day/Month/Year** for better analysis.  
- Flight duration often requires cleaning due to inconsistent formats (e.g., `19h` vs `5m`).  
- Categorical features (`Airline`, `Stops`, `Source`, `Destination`) hold strong predictive power.  
- **OneHotEncoding** is crucial before feeding data into ML models.
