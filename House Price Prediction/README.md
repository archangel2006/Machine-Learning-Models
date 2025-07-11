# 🏠 House Price Prediction Model using Ridge Regression

This project aims to build a **regression-based machine learning model** to predict **median house prices** in California. It uses the **California Housing Dataset** and compares **Linear**, **Ridge**, and **Lasso** Regression models. The final model selected is **Ridge Regression** for its performance and generalization capability.

---

## 📌 Objective

To predict housing prices based on factors like income, house age, population density, and location, and evaluate the model’s performance using real-world regression metrics and visualizations.

---

## 📂 Dataset

- **Source**: `sklearn.datasets.fetch_california_housing`
- **Target Variable**: `MedHouseVal` (Median house value in $100,000s)
- **Features**:
  - `MedInc`: Median Income
  - `HouseAge`: Median house age
  - `AveRooms`: Average number of rooms
  - `AveBedrms`: Average number of bedrooms
  - `Population`: Block population
  - `AveOccup`: Average occupancy
  - `Latitude`, `Longitude`: Location coordinates

---

## 🔍 Exploratory Data Analysis (EDA)

- Inspected data types, null values, and summary statistics.
- Visualized target variable distribution — it is **right-skewed**.
- Identified outliers in the target using **boxplots**.
- Decided to **retain outliers** to ensure model learns from high-value homes.

---

## ⚙️ Preprocessing

- **StandardScaler** applied to input features.
- Dataset split into **training and test sets**.
- Used **RidgeCV** for automated alpha selection in Ridge Regression.

---

## 🧠 Models Compared

| Model      | RMSE  | MAE   | R² Score |
|------------|-------|-------|----------|
| Linear     | 0.745 | 0.533 | 0.575    |
| **Ridge**  | **0.745** | **0.533** | **0.576** |
| Lasso      | 0.746 | 0.533 | 0.574    |

✅ **Ridge Regression** was selected for its better R² score and robustness to multicollinearity.

---

## 📈 Evaluation

**Metrics used**:
- RMSE (Root Mean Squared Error)
- MAE (Mean Absolute Error)
- R² Score (Explained Variance)

**Visualizations**:
- 📊 Actual vs Predicted Scatter Plot
- 📉 Residuals Distribution Plot
- 📌 Feature Importance (Model Coefficients)

---

## 🔢 Final Model

- **Model**: Ridge Regression
- **Scaler**: StandardScaler
- **Best Alpha**: `1.0`



MIT License

Copyright (c) 2025 [Archangel]

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights   
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell     
copies of the Software, and to permit persons to whom the Software is         
furnished to do so, subject to the following conditions:                      

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.                               

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR    
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,      
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE   
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER        
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, 
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE 
SOFTWARE.
