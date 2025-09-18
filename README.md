# APR_Assignment-1_SVR
# 🌲 Forest Fire Area Prediction using SVM (SVR)

This project demonstrates building and evaluating a **Support Vector Regression (SVR)** model to predict the burnt area of forest fires using the `forestfires.csv` dataset.

---

## 📑 Table of Contents
- [Dataset](#dataset)
- [Data Preprocessing](#data-preprocessing)
- [Model Building and Training](#model-building-and-training)
- [Model Evaluation](#model-evaluation)
- [Visualization](#visualization)
- [Summary and Next Steps](#summary-and-next-steps)

---

## 📂 Dataset
The analysis uses the **`forestfires.csv`** dataset, which contains various meteorological and environmental attributes related to forest fires.

---

## 🛠️ Data Preprocessing
- Checked for missing values (**none found**).
- Identified and one-hot encoded categorical columns (`month`, `day`).
- Scaled numerical features using **StandardScaler**.

---

## 🤖 Model Building and Training
- Split the data into training and testing sets (**80/20 split**).
- Initially attempted **SVC**, but since the target variable (`area`) is continuous, it caused a `ValueError`.
- Switched to **SVR (Support Vector Regressor)** for regression task.
- Trained the SVR model on the training dataset.

---

## 📊 Model Evaluation
The model was evaluated using **Mean Squared Error (MSE)** and **R-squared (R²)**:

- **Mean Squared Error (MSE):** `2.95`  
- **R-squared (R²):** `-0.013`

➡️ The **negative R²** indicates that the model performs worse than simply predicting the mean of the target variable.

---

## 📈 Visualization
- A **scatter plot** was generated to visualize the **actual vs. predicted burnt area** values.  
  - The plot showed poor alignment, confirming the low model performance.

---

## ✅ Summary and Next Steps

### 🔍 Key Findings
- Dataset contained **no missing values**.  
- Target variable `area` is **continuous**, requiring regression instead of classification.  
- The **SVR model** achieved:
  - `MSE ≈ 2.95`
  - `R² ≈ -0.01`

### 🚀 Insights & Future Work
- The **negative R²** suggests that the SVR model needs improvement.  
- Possible next steps:
  - Hyperparameter tuning (e.g., kernel, C, epsilon).
  - Feature engineering (log-transforming `area`, interaction terms, etc.).
  - Trying alternative regression algorithms (Random Forest, Gradient Boosting, Neural Networks).
  - Handling skewed distribution of `area` (most values are zero/small).

---

## 📌 Requirements
To run this project, install the required libraries:

```bash
pip install pandas numpy matplotlib scikit-learn
