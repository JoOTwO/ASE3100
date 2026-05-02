# 📊 PCA Implementation

## 📌 Overview

This project implements **Principal Component Analysis (PCA)** using NumPy.

The goal is to understand how data can be reduced from higher dimensions to lower dimensions while preserving important information.

---

## ⚙️ Method

The PCA process:

1. Center the data
2. Compute covariance matrix
3. Perform eigen decomposition
4. Select principal component (largest eigenvalue)
5. Project data onto new axis

---

## 💻 Code

```python
X_c = X - X.mean(axis=0)
cov = np.cov(X_c, rowvar=False)

eigvals, eigvecs = np.linalg.eig(cov)
pc1 = eigvecs[:, np.argmax(eigvals)]

X_pca = X_c @ pc1
```

---

## 📈 Result

* Reduced 2D data → 1D
* Preserved most of the variance in the data

---

## 🧠 What I Learned

* PCA finds directions of maximum variance
* Eigenvectors define new coordinate axes
* Dimensionality reduction can simplify data while keeping key information

---

## 🎯 Motivation

This concept is useful in aerospace applications such as:

* Sensor data analysis
* Noise reduction
* State estimation

---
