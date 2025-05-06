# 7th_day_task-

# Task 7: Support Vector Machines (SVM) - Binary Classification

This project demonstrates the use of **Support Vector Machines (SVM)** for binary classification on a simulated bank marketing dataset. The workflow includes data preprocessing, model training (linear and RBF kernels), hyperparameter tuning, cross-validation, and decision boundary visualization.

---

## Dataset Overview

The dataset (`bank_marketing_svm_dataset.csv`) contains **700 customer records** and is used to predict whether a customer subscribed to a term deposit based on various features.

### Features

| Feature     | Description                                      |
|-------------|--------------------------------------------------|
| `Age`       | Customer age (standardized)                      |
| `Balance`   | Account balance/income indicator                 |
| `Duration`  | Duration of last contact (seconds)               |
| `Campaign`  | Contacts performed during this campaign          |
| `Previous`  | Contacts performed before this campaign          |
| `Subscribed`| Target (0 = No, 1 = Yes)                         |

### Dataset Properties

- Samples: `700`
- Features: `5` (excluding target)
- Target: `Subscribed` (binary: 0/1)
- Class Balance: `50% positive`, `50% negative`

---

## 🚀 Project Workflow

### 1. Data Preprocessing
- Loaded CSV data and validated shape and missing values.
- Applied `StandardScaler` to normalize feature values.

### 2. Model Building
- Trained SVM with both **linear** and **RBF kernels** using `scikit-learn`.
- Compared results on training and testing data.

### 3. Cross-Validation
- Used `cross_val_score` to validate models over 5 folds.

### 4. Hyperparameter Tuning
- Applied `GridSearchCV` to find optimal `C` and `gamma` values for RBF.

### 5. Visualization
- Used PCA to project data into 2D and visualized decision boundaries.

---

##  Results Summary

| Model           | Accuracy | Cross-Validation Avg | Best Params           |
|------------------|----------|----------------------|------------------------|
| Linear SVM       | 82.1%    | 81.4%                | C = 1.0 (default)      |
| RBF SVM (tuned)  | 88.6%    | 87.9%                | C = 10, gamma = 0.1    |

- **Best Model**: RBF Kernel SVM with `C=10`, `gamma=0.1`
- **Insight**: RBF handled non-linear patterns better than linear SVM.

---

##  Key Learnings

- Feature scaling is critical for SVM performance.
- RBF kernel provides flexibility for non-linear decision boundaries.
- Cross-validation ensures model generalizability.
- Hyperparameter tuning significantly boosts performance.

---



