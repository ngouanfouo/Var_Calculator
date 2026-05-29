# VaR (Value-at-Risk) Calculator

**Author: Tiayo Durel**

Access the live interactive dashboard here: [https://var-calculator.streamlit.app](https://var-calculator.streamlit.app)

## 📌 Overview

This module contains a user-friendly Python class, `VaR`, designed to compute Value-at-Risk (VaR) through three distinct approaches: Historical, Parametric, and Monte Carlo simulation.

## ✨ Key Capabilities:

1. **Historical VaR**: Leverages the actual historical return distribution to estimate potential losses.
2. **Parametric VaR**: Often referred to as the variance-covariance method. This approach assumes that returns follow a normal distribution.
3. **Monte Carlo Simulation**: Creates thousands of random portfolio return scenarios and constructs an empirical distribution to determine VaR.

## 📚 Required Libraries:

- `yfinance`: Retrieves past stock price data.
- `numpy`: Handles mathematical operations.
- `matplotlib`: Generates charts and visualizations.

## 🛠️ How to Use It:

Create an instance of the `VaR` class by supplying the following information:

- `ticker`: A list of stock symbols in your portfolio.
- `start_date`, `end_date`: The time period from which to pull historical data.
- `rolling_window`: The window size (in trading days) for computing historical VaR.
- `confidence_level`: The probability threshold for VaR (e.g., 0.95 equals 95% confidence).
- `portfolio_val`: The total monetary value of your portfolio.
- `simulations`: The number of random trials to run for the Monte Carlo method.

**Example:**

```python
var_model = VaR(ticker=['AAPL', 'MSFT'], 
                start_date='2020-01-01', 
                end_date='2025-01-01', 
                rolling_window=252, 
                confidence_level=0.95, 
                portfolio_val=1000000, 
                simulations=1000)
