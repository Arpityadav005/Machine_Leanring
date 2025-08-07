# 🧮 Data Interpolation in Python

This project demonstrates three types of data interpolation using Python:
- Linear Interpolation
- Cubic Interpolation
- Polynomial Interpolation

## 📦 Libraries Used
- NumPy
- Matplotlib
- SciPy

## 📈 Interpolation Techniques

### 1. Linear Interpolation
Straight-line estimation between known data points using `np.interp()`.

### 2. Cubic Interpolation
Smooth curves that match all points using `scipy.interpolate.interp1d(kind='cubic')`.

### 3. Polynomial Interpolation
Fits a polynomial curve of a chosen degree using `np.polyfit()` and `np.polyval()`.

## 📌 Use Cases
- Filling missing values in datasets
- Smoothing noisy data
- Generating additional synthetic data points

---

> Feel free to modify this notebook for more advanced interpolation like spline fitting or higher-order polynomials.

