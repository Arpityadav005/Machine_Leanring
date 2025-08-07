# ⚙️ Data Preparation for Machine Learning

This notebook covers **core preprocessing steps** necessary before training a machine learning model. These include:

## 📋 Steps Included

1. Understanding the Problem
2. Data Ingestion
3. Data Preprocessing & Preparation:
    - Missing values
    - Outlier treatment
    - Class imbalance (not covered here)
    - Feature Engineering (creation, modification, selection)
    - Feature Scaling (Standardization, Normalization, Unit Vector)

## 📉 Curse of Dimensionality
When features increase:
- Model training becomes slower.
- Model interpretation becomes complex.
> Solution: Select relevant features through engineering and selection methods.

## 📐 Feature Scaling Techniques

| Technique       | Formula                          | Use Case                           |
|----------------|-----------------------------------|-------------------------------------|
| Standardization | (X - mean) / std                 | ML algorithms (SVM, LR, KNN, etc.) |
| Normalization   | (X - Xmin) / (Xmax - Xmin)       | Deep Learning, PCA                 |
| Unit Vector     | X / ||X||                        | Clustering, Cosine similarity      |

---
