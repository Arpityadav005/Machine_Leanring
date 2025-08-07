# 🔤 Data Encoding for Categorical Features

This notebook demonstrates the different ways to encode categorical features in machine learning using:

## 🚀 Encoding Types

| Type                      | Description                                                    | Use Case                            |
|---------------------------|----------------------------------------------------------------|--------------------------------------|
| One-Hot Encoding           | Converts categories to binary columns                         | Nominal data (no inherent order)     |
| Label Encoding             | Assigns an integer to each category                           | Ordinal if natural order exists      |
| Ordinal Encoding           | Manual category order with encoded ranks                      | Ordered categorical features         |
| Target Guided Encoding     | Uses statistical relation (e.g., mean) to encode categories   | Many unique categories               |

## 🧠 Why Encode?
- ML models require numeric input
- Encoding affects model performance and interpretability
- Choose encoding based on data type and algorithm

---

> 📎 Tip: Avoid one-hot encoding for high-cardinality features — consider target encoding or embeddings instead.
