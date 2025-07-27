# Class Imbalance Handling in Machine Learning

This notebook demonstrates how to handle **imbalanced datasets**, which are common in real-world ML problems like fraud detection, spam filtering, and medical diagnosis.

---

## 🧠 What is Class Imbalance?

When one class (label) appears much more frequently than the other. For example:


---

## ⚙️ Techniques Covered

### 1. **Upsampling**  
Duplicate minority class samples to match the majority.

### 2. **Downsampling**  
Randomly drop majority samples to match the minority.

### 3. **SMOTE (Synthetic Minority Oversampling Technique)**  
Generate **new synthetic samples** for the minority class using k-nearest neighbors.

---

## 🧰 Libraries Used

| Library | Purpose |
|--------|---------|
| `pandas`, `numpy` | Data handling |
| `sklearn.utils.resample` | Sampling (upsample/downsample) |
| `make_classification` | Generating synthetic data |
| `matplotlib.pyplot` | Data visualization |
| `imbalanced-learn (imblearn)` | SMOTE and resampling tools |

---

## 📉 Why Handle Class Imbalance?

If not handled properly, ML models **bias toward the majority class**, giving poor recall and accuracy on the minority class.

---

## 📍 Next Topic: Data Interpolation  
Now that class imbalance is handled, next we’ll explore **how to fill missing or invalid values** using interpolation techniques.

# -----------------------------
# ⚠️ PROBLEM: CLASS IMBALANCE
# -----------------------------
# Real-world datasets often have one class dominating the other.
# Example: Fraud detection - 98% are normal (class 0), 2% are fraud (class 1)
# If not handled, ML models will be biased towards the majority class
# → High accuracy, but poor recall/precision for minority class

# So, let's handle this problem using multiple strategies.
# -----------------------------
# ✅ UPSAMPLING (copy minority samples)
# -----------------------------
# WHY? To balance classes by increasing minority class
# HOW? We duplicate minority samples with replacement
# PROBLEM? Risk of **overfitting**, because it repeats same data points multiple times
# -----------------------------
# ✅ DOWNSAMPLING (drop majority samples)
# -----------------------------
# WHY? To reduce majority class instead of increasing minority
# PROBLEM? We are **losing valuable data**, which can hurt model performance
# -----------------------------
# ✅ SMOTE (Synthetic Minority Oversampling)
# -----------------------------
# WHY? Creates **new synthetic samples** instead of copying
# HOW? Uses k-nearest neighbors to interpolate between minority class points
# PRO? Avoids both overfitting (upsample) and data loss (downsample)
# CON? Might not work well with categorical data or very small minority class
# -----------------------------
# ✅ NOW WHAT? Move to Next Topic: Data Interpolation
# -----------------------------
# Now our class distribution is balanced ✅
# But in real-world datasets, another common issue is:
# ❗ MISSING VALUES (NaN, blank cells)
# So our next topic will be how to handle them using:
# → Data Interpolation (fill missing values using linear, polynomial methods etc.)
---

## 🔄 Why These Techniques?

| Technique     | Why Used | Problem it Solves | Limitation |
|---------------|----------|-------------------|------------|
| **Upsampling** | Increase size of minority class by copying samples | Class imbalance | Overfitting due to repeated rows |
| **Downsampling** | Reduce size of majority class | Class imbalance | Loss of information |
| **SMOTE** | Create new synthetic data points | Balances data while preserving diversity | Not ideal for small datasets or categorical features |

---

## 🧠 Why Move to Next Topic: Data Interpolation?

After handling class imbalance, the next most common problem in datasets is **missing values**.

- Models can’t be trained with `NaN` values
- Missing values can bias or crash your model
- So, we’ll now learn **Data Interpolation** to fill them smartly

📌 Coming Up: `data_interpolation.ipynb`

---

