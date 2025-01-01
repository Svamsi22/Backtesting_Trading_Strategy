# Backtesting_Trading_Strategy

This repository contains the implementation and analysis of the take-home task submitted for the quantitative analyst position. Below are the key details about the project, its components, and how to run the code.

---

## Overview

The project involves developing, implementing, and backtesting trading strategies based on momentum indicators. The objective is to maximize risk-adjusted returns while minimizing potential losses. The strategies and metrics included have been refined based on feedback and additional analysis.

---

## Key Features

### 1. **Data Fetching**
- Data is fetched from Yahoo Finance using the URL method:
  ```java
  private static final String BASE_URL = "https://query1.finance.yahoo.com/v8/finance/chart/%s?range=%s&interval=%s";
  ```
- This ensures efficient retrieval of adjusted close prices for specified stocks and time frames.

### 2. **Trading Strategies**
#### a. **SMA-based Strategy**
- Buy stocks when the price is above the Simple Moving Average (SMA).

#### b. **EWA-based Strategy**
- Buy stocks when the price is above the Exponential Weighted Average (EWA).

#### c. **Combined Strategy**
- Combines SMA and EWA signals.
- Generates buy signals based on the maximum return from either SMA or EWA.

### 3. **Performance Metrics**
- **Sharpe Ratio**: To assess risk-adjusted return.
- **Maximum Drawdown**: To measure potential loss from peak to trough.
- **Annualized Return**: To calculate yearly performance.

### 4. **Key Observations**
- **Best Risk-Adjusted Performance**: Combined Strategy, 1-year time frame, daily frequency (Window Size: 5), Sharpe Ratio = 1.658.
- **Maximizing Returns**: Combined Strategy, 5-year time frame, daily frequency (Window Size: 5), Annualized Return = 19.01%.
- **Minimizing Losses**: Combined Strategy, 1-year time frame, weekly frequency (Window Size: 5), Maximum Drawdown = 0%.

---



## Results

Detailed results and observations are included in the `results/` directory. Key highlights:
- **Best Sharpe Ratio**: Combined Strategy, 1-year time frame, daily frequency, Window Size: 5.
- **Maximum Annualized Return**: Combined Strategy, 5-year time frame, daily frequency, Window Size: 5.
- **Lowest Maximum Drawdown**: Combined Strategy, 1-year time frame, weekly frequency, Window Size: 5.

---

## Future Improvements
- Explore additional indicators (e.g., RSI, Bollinger Bands).
- Include transaction costs in the backtesting.
- Optimize parameters using machine learning models.

---

**Disclaimer**: This project is for educational purposes only. It should not be used for actual trading without further validation and due diligence.
