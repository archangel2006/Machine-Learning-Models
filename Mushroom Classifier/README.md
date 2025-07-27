# 🍄 Mushroom Classification – Edible or Poisonous?

(Date: July 27, 2025)

This project builds and compares multiple classification models to determine whether a mushroom is **edible** or **poisonous** based on its features. The dataset is processed and evaluated using **K-Nearest Neighbors (KNN)**, **Logistic Regression**, and **Random Forest** classifiers. Evaluation metrics such as accuracy, precision, recall, and F1-score are used to compare model performance.

---

## 📌 Objective  
To classify mushrooms as **edible (e)** or **poisonous (p)** based on their categorical features. The goal is to build a robust model that generalizes well and can assist in safe mushroom identification.

---

## 📂 Dataset  
**Source:** [UCI Mushroom Dataset](https://www.kaggle.com/datasets/uciml/mushroom-classification)  
**Target Variable:** `class` (e = edible, p = poisonous)

**Features (after encoding):**
- cap-shape
- cap-surface
- cap-color
- bruises
- odor
- gill-attachment
- gill-spacing
- gill-size
- gill-color  
*(+ several more, total 22 features after encoding)*

---

## 🔍 Exploratory Data Analysis (EDA)
- Checked shape, data types, null values (none found).
- Examined class distribution – fairly balanced.
- Analyzed frequency of each feature's unique values.
- Visualized correlation between selected categorical features and class.
- Inspected label distribution with bar plots.

---

## ⚙️ Preprocessing  
- Label encoding applied to all categorical variables.
- Train-test split using `train_test_split` (test size = 20%).
- Feature scaling using `StandardScaler` (for KNN & Logistic Regression).
- All models trained on the same preprocessed data for fair comparison.

---

## 🧠 Model Comparison

| Model               | Accuracy | Precision | Recall | F1-Score | Notes |
|--------------------|----------|-----------|--------|----------|-------|
| KNN (k=5)           | 91.23%   | 0.90      | 0.92   | 0.91     | Sensitive to feature scaling |
| Logistic Regression | 94.73%   | 0.95      | 0.95   | 0.95     | Strong linear separator |
| Random Forest       | **100%** | 1.00      | 1.00   | 1.00     | Perfect accuracy, robust model |

---

## 📈 Evaluation

### 🔢 Classification Report (Random Forest)

| Metric     | Class e (Edible) | Class p (Poisonous) | Interpretation |
|------------|------------------|----------------------|----------------|
| Precision  | 1.00             | 1.00                 | No false positives |
| Recall     | 1.00             | 1.00                 | No false negatives |
| F1-Score   | 1.00             | 1.00                 | Perfect prediction |
| Support    | 839              | 781                  | Balanced test set |
| Accuracy   | —                | —                    | **100% overall** |
| Macro Avg  | —                | —                    | Precision: 1.00, Recall: 1.00, F1: 1.00 |
| Weighted Avg| —               | —                    | All classes well-represented |

---

### 🧮 Confusion Matrix (Random Forest)

| Actual \ Pred | Pred e | Pred p | Interpretation |
|---------------|--------|--------|----------------|
| **Actual e**  | 839    | 0      | All edible mushrooms correctly identified |
| **Actual p**  | 0      | 781    | All poisonous mushrooms correctly identified |

---


