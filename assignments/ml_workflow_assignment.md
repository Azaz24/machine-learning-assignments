# 📊 Machine Learning Workflow Assignment


---

# 🧠 Problem Statement

The objective is to build a machine learning model that predicts whether a customer will make a repeat purchase within 30 days based on their past purchase behavior.

---

# 📊 Dataset Overview

The dataset contains customer transaction history with the following features:

* `customer_id`: Unique identifier for each customer
* `order_count_last_90d`: Number of orders placed in the last 90 days
* `avg_order_value`: Average spending per order (INR)
* `days_since_last_order`: Recency of last purchase
* `repeat_purchase_flag`: Target variable (1 = Yes, 0 = No)
* `discount_used_on_repeat_order`: Discount applied on repeat purchase

---

# 🏷️ Task 1: Label Identification & Data Leakage Detection

## 🎯 Objective

To identify the correct target variable and detect features that could introduce data leakage.

## ✅ Label Identification

**Label:** `repeat_purchase_flag`
**Justification:** This variable represents the outcome to be predicted — whether a customer makes a repeat purchase within 30 days.

## ⚠️ Data Leakage Detection

**Leakage Column:** `discount_used_on_repeat_order`
**Justification:** This column contains information that is only available after the repeat purchase has occurred, making it unsuitable for model training.

---

# 🏷️ Task 2: Machine Learning Data Preparation

## 🎯 Objective

To prepare a clean and unbiased dataset before training the model.

---

## 🔧 Step 1: Data Cleaning (Removing Leakage)

* Removed the `discount_used_on_repeat_order` column
* Ensured that the model only uses historical data

**Impact:**
Prevents unrealistic predictions and ensures model reliability.

---

## 🔧 Step 2: Feature and Target Separation

* Defined input features (X) and target variable (y)
* Excluded non-informative columns like `customer_id`

**Impact:**
Ensures that the model focuses only on relevant predictive features.

---

## 🔧 Step 3: Train-Test Split

* Split dataset into training and testing sets (80-20)

**Impact:**
Allows evaluation of model performance on unseen data.

---

# ⚙️ Model Implementation

* Used **Gradient Boosting Classifier**
* Trained model on customer behavioral features
* Predicted repeat purchase likelihood

---

# 📊 Results & Interpretation

* The model achieved **100% accuracy (1.0)** on the test dataset.
* All test samples were predicted correctly.

⚠️ **Note:**  
The dataset is very small, which may lead to overly optimistic performance. The model may not generalize well to larger, real-world data.

**Interpretation:**  
While the model captures customer behavior effectively, a larger dataset is required to validate its robustness and ensure reliable performance in real-world scenarios.
---

# 🎯 Key Learnings

* Data leakage must be removed to ensure valid model performance
* Customer behavior features (recency, frequency, monetary value) are strong predictors
* Proper data preparation is critical before model training
* Train-test split ensures unbiased evaluation

---

# 🚀 Conclusion

This project demonstrates how machine learning can be applied to predict customer retention. By using historical purchase data and proper preprocessing techniques, the model provides actionable insights that can improve marketing strategies and customer engagement.

---

# 🔗 Submission Instructions

* File Name: `ml_workflow_assignment.md`
* Upload to: `assignments/` folder in GitHub repository
* Share the repository link

---
