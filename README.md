# Walmart_Sales_Prediction

Predicting weekly sales across Walmart stores using various machine learning algorithms with a focus on seasonality, holidays, and economic indicators.

## Introduction

Walmart, one of the largest retailers in the United states, needs accurate sales predictions to manage inventory and demand effectively. This project aims to develop machine learning models to forecast **weekly sales** across 45 Walmart stores using historical data that includes holiday flags, economic factors, and seasonal trends.

## 📊 Dataset

| Column Name     | Description                                           |
|-----------------|-------------------------------------------------------|
| `Store`         | Store ID                                              |
| `Date`          | Week of sales                                         |
| `Weekly_Sales`  | Sales amount for the given week and store            |
| `Holiday_Flag`  | 1 for holiday week, 0 for non-holiday week           |
| `Temperature`   | Temperature of the region                             |
| `Fuel_Price`    | Regional fuel cost                                    |
| `CPI`           | Consumer Price Index                                  |
| `Unemployment`  | Regional unemployment rate                            |

- **Important Holidays Considered:** Super Bowl, Labour Day, Thanksgiving, Christmas
- **Holiday weights:** Holiday weeks are given 5x the weight of non-holiday weeks.

## Exploratory Data Analysis

**Univariate Analysis:**
-'Weekly_Sales' is right skewed
-'CPI' and 'Fuel_price' show bimodal distributions.
**Seasonal Trends:**
-Sales spike in **Winter** (Nov & Dec).
-Holiday weeks have higher sles.
**Correlation Heatmap:**
-Revealed weak to moderate correlations among features and target.

## 🤖 Models and Results

| Model                   | Train Accuracy | Test Accuracy | Best Parameters                                 |
|------------------------|----------------|---------------|--------------------------------------------------|
| **Linear Regression (Poly)** | 97.9%         | 96.1%        | `degree=3`                                       |
| **K-Nearest Neighbors**     | 100%          | 93.8%        | `n_neighbors=5`, `metric=manhattan`, `weights=distance` |
| **Random Forest Regressor** | 99.4%         | **95.7%**    | Default params (used OneHotEncoding)             |

## ✅ Conclusion

- **Random Forest Regressor** provided the best performance (Test R² ≈ **95.71%**) and is recommended for deployment.
- Seasonality and holidays significantly impact sales.
- Economic indicators (CPI, Fuel Price, Unemployment) had moderate influence.

