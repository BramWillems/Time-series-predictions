# AI Exploration Proposal

**Title:** Predicting Next-Day Stock Price Movements Using Recent Market Data

## 1. Context & Motivation

Financial markets are dynamic systems where prices fluctuate continuously due to a mix of temporal trends, market sentiment, and external events. Understanding how to predict short-term stock movements provides insight into time-sensitive data modeling — a core skill in AI and data science.

This exploration focuses on predicting whether a stock's closing price will go up or down the next day, based on the past week's performance. The project highlights key principles of temporal feature engineering and supervised learning for sequential data.

## 2. Research Question

Can a machine learning model predict whether a stock's price will rise or fall the next day using only the last 7 days of historical price data?

## 3. Dataset

- **Source:** Yahoo Finance API (`yfinance` Python library)
- **Example Symbol:** AAPL (Apple Inc.) or TSLA (Tesla, Inc.)
- **Period:** Last 2–3 years of daily stock data
- **Main Features:**
  - Date
  - Open, High, Low, Close, Volume
- **Target Variable:** Binary label — 1 if the next day's closing price is higher than today's, 0 otherwise.

## 4. Methodology

### Step 1: Data Preparation
- Collect daily stock data for a single stock.
- Compute percentage changes in closing prices.
- Create lag features for the past 7 days (Close[t−1] … Close[t−7]).
- Define the binary target (up/down).

### Step 2: Model Development
Train and compare:
- **Baseline:** Logistic Regression (interpretable linear model)
- **Alternative:** Random Forest or LSTM (nonlinear temporal models)

### Step 3: Evaluation
**Metrics:**
- Accuracy
- Precision, Recall, F1-score
- Confusion Matrix (to visualize prediction distribution)

### Step 4: Visualization
- Plot predicted vs. actual "up/down" movements.
- Optional: feature importance plot for interpretability.

## 5. Expected Learning Outcomes

By completing this 1–2 day exploration, I will:
- Understand how temporal dependencies affect predictive performance.
- Practice feature engineering for time-sensitive data.
- Compare linear vs. nonlinear models on sequential data.
- Reflect on prediction limits in noisy, real-world financial data.

## 6. Ethical Reflection

While financial forecasting can have commercial applications, this experiment is conducted purely for educational purposes. It highlights the risks of overfitting and the importance of not relying on AI predictions for real-world trading without rigorous validation.

## 7. Deliverables

- Cleaned dataset (CSV or DataFrame).
- Python notebook (`.ipynb`) with modeling workflow.
- Short reflection report including:
  - Model results and evaluation metrics
  - Discussion of challenges and insights about temporal prediction

## 8. Duration

**Estimated Time:** 1–2 days
- **Day 1:** Data exploration and feature creation
- **Day 2:** Model training, evaluation, and reflection
