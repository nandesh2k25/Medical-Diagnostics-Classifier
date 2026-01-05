# 🎗️ Breast Cancer Detection using SVM

## 📌 Project Overview
This repository contains a machine learning pipeline to classify breast cancer tumors as **Malignant** (Cancerous) or **Benign** (Non-cancerous). Using the Wisconsin Breast Cancer Diagnostic dataset, I implemented a Support Vector Machine (SVM) classifier to assist in clinical decision-making.

In medical diagnostics, the cost of a **False Negative** (missing a cancer case) is extremely high. Therefore, this project focuses on optimizing **Recall** alongside overall accuracy.

## 📊 Dataset Information
* **Source:** `sklearn.datasets.load_breast_cancer()`
* **Instances:** 569
* **Features:** 30 (Radius, Texture, Perimeter, Area, Smoothness, etc.)
* **Classes:** Benign (357), Malignant (212)



## 🛠️ Data Science Pipeline

### 1. Exploratory Data Analysis (EDA)
- Analyzed feature correlations using Heatmaps.
- Visualized class distribution to check for data imbalance.
- Identified "Mean Radius" and "Mean Concave Points" as the strongest predictors.

### 2. Preprocessing
- **Feature Scaling:** Since SVM is a distance-based algorithm, I applied `StandardScaler` to ensure all features contribute equally to the decision boundary.
- **Train-Test Split:** Utilized an 80/20 split with `random_state` for reproducibility.



### 3. Support Vector Machine (SVM) Implementation
I utilized the RBF (Radial Basis Function) kernel to handle potential non-linear relationships in the tumor data.
- **Kernel:** RBF
- **C Parameter:** Optimized to balance margin width and misclassification.

## 📈 Performance & Cross-Validation
To ensure the model is robust and stable, I performed **5-Fold Cross-Validation**.

| Metric | Single Split Score | Cross-Validation (Avg) |
| :--- | :---: | :---: |
| **Accuracy** | 97.4% | 96.8% |
| **Recall (Malignant)** | 96.2% | 95.9% |
| **F1-Score** | 0.97 | 0.96 |



## 🚀 Key Insights
- **Why SVM?** SVM is highly effective in high-dimensional spaces, making it perfect for the 30-feature Breast Cancer dataset.
- **Scaling is Critical:** Without `StandardScaler`, the SVM performance dropped significantly (from 97% to ~91%).

## 📂 How to Run
1. Clone the repo:
   ```bash
   git clone [https://github.com/yourusername/Breast-Cancer-Detection-SVM.git](https://github.com/yourusername/Breast-Cancer-Detection-SVM.git)"# Medical-Diagnostics-Classifier" 
