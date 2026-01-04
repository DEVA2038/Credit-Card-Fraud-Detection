# 💳 Fraud Detection using Machine Learning Pipeline

This project implements an **end-to-end fraud detection pipeline** using machine learning.  
It covers **data loading, exploratory data analysis (EDA), preprocessing, class imbalance handling, model training, evaluation, and comparison**.

The pipeline is designed to handle **highly imbalanced fraud datasets** and evaluates multiple classifiers to identify the best-performing model.

---

## 🚀 Project Overview

Fraud detection is a critical problem in financial systems where fraudulent transactions are extremely rare compared to legitimate ones.  
This project builds a **robust and modular fraud detection system** that:

- Handles **class imbalance** using sampling techniques
- Trains multiple ML models
- Evaluates performance using **precision, recall, F1-score, ROC-AUC, and PR-AUC**
- Visualizes results using professional plots

---

## 📂 Dataset

- **File Name:** `fraudTest.csv`
- **Target Column:** `is_fraud` (renamed internally to `Class`)
  - `0` → Not Fraud
  - `1` → Fraud
- **Amount Column:** `amt` (renamed to `Amount`)

### Selected Features
The pipeline uses the following numerical features:
- `Amount`
- `lat`
- `long`
- `city_pop`
- `unix_time`
- `merch_lat`
- `merch_long`

⚠️ If some features are missing, the pipeline automatically adapts and uses available ones.

---

## 🧹 Data Preprocessing

### ✔ Feature Scaling
- **StandardScaler** is applied to numerical features

### ✔ Class Imbalance Handling
Two strategies are supported:
- **Random Under Sampling**
- **SMOTE (Synthetic Minority Oversampling Technique)**

(Default: **Under Sampling**)

---

## 📊 Exploratory Data Analysis (EDA)

The pipeline performs:
- Class distribution analysis
- Fraud rate calculation
- Feature statistics summary
- Visualization of class imbalance using bar plots

---

## 🤖 Machine Learning Models Used

The following models are trained and evaluated:

- **Logistic Regression**
- **Decision Tree Classifier**
- **Random Forest Classifier**
- **Gradient Boosting Classifier**

Several models use **class_weight='balanced'** to further address imbalance.

---

## 📈 Model Evaluation Metrics

Each model is evaluated using:

- **Precision**
- **Recall**
- **F1-Score**
- **ROC-AUC**
- **Precision-Recall AUC**

### Visualizations:
- Confusion Matrix Heatmaps
- ROC Curves
- Precision–Recall Curves
- Model comparison bar charts

---

## 🏆 Model Comparison & Selection

- All models are ranked based on **F1-score**
- A summary table compares:
  - Precision
  - Recall
  - F1-score
  - ROC-AUC
  - PR-AUC
- The **best-performing model** is automatically recommended

---

## 🛠️ Technologies Used

- **Python**
- **Pandas**
- **NumPy**
- **Matplotlib**
- **Seaborn**
- **Scikit-learn**
- **Imbalanced-learn (imblearn)**

---

## ▶️ How to Run the Project

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/your-username/fraud-detection-ml.git
cd fraud-detection-ml
