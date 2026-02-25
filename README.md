#  Machine Learning Challenge: Denoising & Classification

---

## 📋 Overview
This project consists of two specialized machine learning tasks: **Multi-Label Classification** and **Image Noise Removal**. The core focus is to demonstrate how different algorithms handle noisy data and complex labeling.

---

## 🛠 Task 1: Multi-Label Classification
**Goal:** Classify MNIST digits based on multiple properties: parity (**Is_Odd**) and value (**Greater_than_5**).

### 🚀 Implementation & Comparison
We compared two powerful classifiers: **Random Forest** and **K-Nearest Neighbors (KNN)** using Multi-Output wrappers.

| Model | F1-Score | Samples Avg | Performance |
| :--- | :--- | :--- | :--- |
| **KNN** | **0.98** | **0.69** | ✅ **Top Precision** |
| **Random Forest** | 0.97 | 0.68 | Solid Baseline |

<img width="691" height="470" alt="image" src="https://github.com/user-attachments/assets/cc55c2d8-da73-4837-b2e0-00b5aacc200b" />
*[Performance Metrics: RF vs KNN]*

**Key Insights:**
* **KNN Excellence:** The KNN model achieved a near-perfect F1-score of **0.98**, showing superior capability in identifying the specific boundaries of our multi-label categories.
* **Consistency:** Both models maintained a stable "Samples Average" (around 0.68-0.69), proving robust performance across the entire test set.

---

## 🧪 Task 2: Noise Removal (Denoising)
**Goal:** Restore original "clean" images from digits corrupted by random synthetic noise.

### 📈 Experimental Results
We evaluated three approaches using **Mean Squared Error (MSE)** to measure restoration quality.

| Model | Status | MSE Score | Performance |
| :--- | :--- | :--- | :--- |
| **Noisy Baseline** | Pre-processing | **0.0213** | Corrupted Data |
| **Linear Regression** | Denoised | **0.0073** | ✅ **Best Performer** |
| **KNN (k=3)** | Denoised | **0.0228** | ⚠️ Noise Increase |
| **Random Forest** | Denoised | **0.0350** | ❌ High Error |

**Key Findings:**
* **Optimal Solution:** **Linear Regression** achieved a **65.7% reduction** in noise, proving that simple linear mapping is highly effective for MNIST pixel restoration.
* **Analysis:** Despite KNN's success in classification (Task 1), it struggled with pixel-perfect denoising, highlighting that the "best" model depends entirely on the specific task.

---

## 💻 Technical Stack

<p align="left">
  <img src="https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54" alt="Python" />
  <img src="https://img.shields.io/badge/numpy-%23013243.svg?style=for-the-badge&logo=numpy&logoColor=white" alt="NumPy" />
  <img src="https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white" alt="Scikit-Learn" />
  <img src="https://img.shields.io/badge/Matplotlib-%23ffffff.svg?style=for-the-badge&logo=Matplotlib&logoColor=black" alt="Matplotlib" />
</p>

- **Language:** Python 3.x
- **Core Libraries:** `Scikit-Learn`, `NumPy`, `Matplotlib`, `Scikit-Image`
- **Dataset:** MNIST Handwritten Digits

---
**Prepared as part of the Machine Learning Challenge.**
