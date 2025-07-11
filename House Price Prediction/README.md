# 🏠 House Price Prediction Model

This project focuses on building a **regression model** to predict **median house prices** using California Housing Dataset. The final model is trained using **Ridge Regression**, after evaluating and comparing with Linear and Lasso regression models.

---

## 📌 Objective

To create a machine learning model that can accurately predict housing prices based on various features such as median income, house age, average rooms, etc.

---

## 📂 Dataset

- **Source**: California Housing Dataset (`sklearn.datasets.fetch_california_housing`)
- **Target**: `MedHouseVal` (Median house value in units of $100,000)
- **Features**:
  - `MedInc` (Median Income)
  - `HouseAge`, `AveRooms`, `AveBedrms`
  - `Population`, `AveOccup`
  - `Latitude`, `Longitude`

---

## 🔍 Exploratory Data Analysis (EDA)

- Histograms and boxplots were used to inspect **target distribution and outliers**.
- Outliers were identified but **retained** to ensure the model learns from high-value houses as well.

---

## 🧠 Models Compared

| Model           | RMSE   | MAE   | R² Score |
|----------------|--------|-------|----------|
| Linear         | 0.74   | 0.53  | 0.57     |
| **Ridge**      | **0.74** | **0.53** | **0.58**     |
| Lasso          | 0.74   | 0.53  | 0.57     |

✅ **Ridge Regression** was chosen due to slightly better generalization and its robustness against multicollinearity.

---

## 📈 Evaluation

- **Evaluation Metrics**:
  - RMSE (Root Mean Squared Error)
  - MAE (Mean Absolute Error)
  - R² Score

- **Visualizations**:
  - Actual vs Predicted Scatter Plot
  - Residual Distribution Plot
  - Feature Importance via Coefficient Bar Chart

---

## 🔢 Final Model

- **Model**: Ridge Regression
- **Alpha (regularization)**: `1.0` (chosen via cross-validation)
- **Scaler**: StandardScaler (fit on training data)

Model and scaler are saved using `joblib`:
```python
joblib.dump(model, 'ridge_model.pkl')
joblib.dump(scaler, 'scaler.pkl')
