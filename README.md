# Portfolio Risk Analytics and VaR Model Validation

## Overview

This project implements a quantitative risk analytics framework for evaluating the downside risk of a diversified investment portfolio. Using historical market data, the framework estimates potential portfolio losses through multiple Value-at-Risk (VaR) methodologies, measures tail risk using Expected Shortfall (CVaR), and performs basic VaR backtesting to assess model performance.

The project demonstrates fundamental concepts used in portfolio risk management, including return distribution analysis, statistical risk modeling, Monte Carlo simulation, and model validation.

---

## Objective

The primary objective of this project is to quantify portfolio downside risk and estimate potential losses under normal market conditions. The project compares different VaR estimation techniques and evaluates their effectiveness in measuring risk exposure across a diversified portfolio.

---

## Key Features

* Historical Value-at-Risk (VaR) Estimation
* Parametric (Variance-Covariance) VaR Estimation
* Monte Carlo Simulation-Based VaR
* Expected Shortfall (CVaR) Calculation
* Portfolio Return and Volatility Analysis
* VaR Backtesting through Breach Analysis
* Risk Distribution Visualization
* Automated Market Data Retrieval from Yahoo Finance

---

## Methodology

### 1. Data Collection

Historical daily price data for multiple assets is downloaded using the Yahoo Finance API through the `yfinance` library.

### 2. Portfolio Construction

A diversified portfolio is created using randomly generated asset weights normalized to sum to one.

### 3. Return Computation

Daily percentage returns are calculated for each asset and aggregated into portfolio-level returns using weighted averaging.

### 4. Risk Estimation

The following risk metrics are computed:

#### Historical VaR

Calculates the 5th percentile of historical portfolio returns to estimate the maximum expected loss at a 95% confidence level.

#### Parametric VaR

Assumes normally distributed returns and estimates VaR using portfolio mean returns and volatility.

#### Monte Carlo VaR

Generates thousands of simulated return scenarios using a normal distribution and estimates VaR from the simulated loss distribution.

#### Expected Shortfall (CVaR)

Measures the average loss beyond the VaR threshold, providing insight into extreme downside risk.

### 5. VaR Backtesting

The model is evaluated by comparing the observed frequency of VaR breaches against the expected breach frequency implied by the confidence level.

---

## Technologies Used

* Python
* Pandas
* NumPy
* SciPy
* Matplotlib
* yFinance

---

## Results

The project generates:

* Portfolio Return Statistics
* Historical VaR
* Parametric VaR
* Monte Carlo VaR
* Expected Shortfall (CVaR)
* VaR Breach Rate
* Portfolio Risk Visualizations

These metrics provide a comprehensive view of portfolio risk exposure and downside vulnerability.

---

## Applications

This framework can be used for:

* Portfolio Risk Assessment
* Investment Risk Monitoring
* Quantitative Finance Learning
* Market Risk Analysis
* Risk Management Research
* Financial Data Analytics

---

## Future Enhancements

Potential extensions include:

* Kupiec Proportion of Failures Test
* Christoffersen Backtesting Framework
* Stress Testing and Scenario Analysis
* Dynamic Portfolio Rebalancing
* Efficient Frontier Integration
* GARCH-Based Volatility Modeling
* Interactive Dashboard Development

---

## Conclusion

This project provides a practical implementation of commonly used market risk measurement techniques. By combining Historical VaR, Parametric VaR, Monte Carlo Simulation, Expected Shortfall, and VaR Backtesting, the framework offers a comprehensive introduction to quantitative portfolio risk analytics and model evaluation.

---

## Author

**Sayan Das**  
Indian Institute of Technology (IIT) Kharagpur
