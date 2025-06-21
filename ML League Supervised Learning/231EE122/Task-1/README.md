# Blueberry Yield Prediction – Supervised Regression Project

**Name** : Jyotirmaya Mallick  
**Roll Number** : 231EE122  
**Kaggle Username** : [Aromatic_Isopod](https://www.kaggle.com/jam2004)

---

## Task

Develop a regression model to **predict blueberry yield** using supervised learning techniques.

---

## 📊 Project Workflow

### 1. Exploratory Data Analysis (EDA) & Feature Engineering
- Verified that there were **no missing values** or **categorical variables**.
- Analyzed the distribution of the **target variable (`Yield`)** — found to be **approximately normal**, so no transformation was needed.
- Calculated correlation between **independent variables** and the **target**.
- Plotted a **correlation heatmap** to detect and reduce **multicollinearity**:
  - Found that all **temperature-related features** and **rain-related features** were highly correlated with each other.
  - Removed redundant columns

---

## ⚙️ Model Performance (Mean Absolute Error - MAE)

| Model                        | MAE                        |
|-----------------------------|----------------------------|
| Linear Regression           | 267.98                     |
| Ridge Regression            | 267.99                     |
| Lasso Regression            | 267.97                     |
| ElasticNet                  | 352.69                     |
| Support Vector Regressor    | 620.78                     |
| K-Nearest Neighbors (KNN)   | 312.01                     |
| Decision Tree               | 244.53                     |
| Random Forest               | 241.86                     |
| Gradient Boosting           | 244.25                     |
| AdaBoost                    | **237.78** 🔥              |
| XGBoost                     | 242.07                     |
| LightGBM                    | 243.25                     |

> ℹ️ All models were evaluated using **cross-validation** to avoid overfitting.

---

## 🔧 Optimization & Ensembling

- Used **Optuna** for **hyperparameter tuning**, maximizing model performance.
- Found that **tree-based models** significantly outperformed linear ones.
- To further reduce MAE:
  - Created an **ensemble** using top-performing models.
  - Implemented both **weighted average ensembling** and **stacked regression**.
- The **best Kaggle score** was achieved using a **weighted average ensemble** of:
  - **Random Forest**
  - **XGBoost**
  - **AdaBoost**

---
