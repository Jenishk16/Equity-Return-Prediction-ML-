# Equity Return Prediction using Machine Learning

## Problem Statement

Financial markets are highly noisy and predicting short-term price movements is extremely challenging.
This project investigates whether simple historical indicators such as past returns, momentum, and volatility contain any predictive signal for future stock returns.

The goal is not necessarily to achieve high prediction accuracy, but to evaluate whether these basic features provide any statistically meaningful signal for forecasting returns.

---

## Project Goal

To test whether **historical return-based features** can help predict future returns using a **Linear Regression baseline model**.

---

## Dataset

* Source: Yahoo Finance
* Data Type: Daily stock price data
* Period: Historical daily price data for a selected equity

---

## Feature Engineering

Financial markets often exhibit short-term patterns such as **momentum** and **volatility clustering**.
To capture these effects, the following features were created:

1. Daily return
2. 5-day momentum
3. Moving average ratio (5-day / 10-day)
4. 5-day rolling volatility

These features are derived only from **past information** to avoid look-ahead bias.

---

## Model

A **Linear Regression model** is used as a baseline.

Linear regression estimates the relationship between the engineered features and the future return.

The objective is to determine whether these simple features contain any predictive information.

---

## Evaluation Metrics

### Mean Squared Error (MSE)

Measures the average squared difference between predicted and actual returns.

### R² Score

Indicates how much variance in returns is explained by the model.

In financial return prediction, R² values are often **close to zero** due to the noisy nature of markets.

---

## Key Findings

* Feature engineering slightly improves the model's fit on training data.
* However, the **out-of-sample predictive power remains very weak**.
* This result is consistent with the **efficient market hypothesis**, which suggests that short-term returns are difficult to predict using simple historical features.

