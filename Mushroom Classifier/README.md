# 🍄 Mushroom Classifier: Edible or Poisonous?

A machine learning project to classify mushrooms as **edible** or **poisonous** based on their physical characteristics. Built using supervised learning models like **K-Nearest Neighbors (KNN)**, **Logistic Regression**, and **Random Forest**, this project aims to find the most accurate and reliable classifier for mushroom safety.

---

## 📌 Objective

To develop a machine learning model that can **predict the edibility of mushrooms** using a variety of physical attributes such as odor, cap shape, gill size, and color. The goal is to **compare multiple classifiers** and determine the most effective one for this task.

---

## 🧠 Models Used

- ✅ **K-Nearest Neighbors (KNN)**
- ✅ **Logistic Regression**
- ✅ **Random Forest Classifier**

---

## 📂 Dataset

- **Source**: [Kaggle – Mushroom Classification Dataset](https://www.kaggle.com/datasets/uciml/mushroom-classification)
- **Size**: ~8,000 samples
- **Features**: 22 categorical features
- **Target Variable**:
  - `e` = Edible
  - `p` = Poisonous

---

## 🧪 Project Workflow

### 1. Data Loading & Exploration
- Checked feature names and unique values
- Visualized class distribution (edible vs poisonous)
- Identified important categorical features

### 2. Preprocessing
- Label encoding for all categorical features
- Handled missing values (`?` in `stalk-root`)
- Train-test split (80/20)
- Feature scaling applied (for KNN)

### 3. Model Training
Trained all three classifiers on the training set:
- **KNN** (with scaling)
- **Logistic Regression** (no scaling)
- **Random Forest** (no scaling)

### 4. Evaluation
- Metrics: **Accuracy, Precision, Recall, F1-Score**
- Confusion matrix visualized for each model

### 5. Comparison & Conclusion
| Metric         | KNN   | Logistic Regression | Random Forest |
|----------------|-------|----------------------|----------------|
| Accuracy       | 1.00  | 0.9477               | 1.00           |
| Precision      | 1.00  | 0.9439               | 1.00           |
| Recall         | 1.00  | 0.9476               | 1.00           |
| F1-Score       | 1.00  | 0.9458               | 1.00           |

- **Best Models**: KNN and Random Forest (perfect classification)
- **Top Feature**: `odor` was the most informative feature for predicting toxicity.

---

## 📌 Key Insights

- Mushrooms with certain odors are highly predictive of being poisonous.
- Tree-based models and distance-based models performed perfectly due to clear class separability.
- Logistic Regression had slightly lower performance due to its linear nature.
