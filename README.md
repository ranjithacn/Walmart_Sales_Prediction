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

