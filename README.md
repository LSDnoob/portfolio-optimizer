# Portfolio Optimization Using the Efficient Frontier

## Overview

This project implements Mean-Variance Portfolio Optimization to construct an optimal portfolio using historical stock data. The goal is to maximize returns while minimizing risk by leveraging Modern Portfolio Theory (MPT) and visualizing the Efficient Frontier.

## Key Features

- Fetches historical stock data using yfinance
- Computes daily returns, mean returns, and covariance matrix
- Uses Scipy's SLSQP optimizer for portfolio optimization
- Visualizes the Efficient Frontier
- Analyzes optimal portfolio weights for different target returns

## Libraries used

- yfinance (for fetching stock data)
- pandas (for data handling)
- numpy (for numerical computations)
- scipy.optimize (for portfolio optimization)
- matplotlib (for visualization)

## Data & Stock Selection

The portfolio consists of five stocks across different sectors to ensure diversification:

- AAPL (Apple Inc.) – Technology
- JPM (JPMorgan Chase) – Financials
- XOM (ExxonMobil) – Energy
- PG (Procter & Gamble) – Consumer Goods
- NVDA (NVIDIA) – Semiconductors

## How it works

1. Data Collection & Processing
- Download historical stock prices (closing prices) from Yahoo Finance.
- Computes daily percentage returns.
- Calculates mean returns and covariance matrix.

2. Portfolio Optimization
- Uses Mean-Variance Optimization to construct portfolios for different target returns.
- Solves for minimum variance portfolios given a required return using scipy.optimize.minimize.
- Ensures portfolio weights sum to 1 and are non-negative (long-only constraint).

3. Efficient Frontier Visualization
- Plots the Efficient Frontier, which represents the set of optimal portfolios offering the best possible return for a given level of risk.
- Displays portfolio weights for selected points on the frontier.

## Sample Output

- Efficient Frontier Graph: A plot showing optimal risk-return combinations.
- Portfolio Weights: Example allocations for different target returns.

## Possible Enhancements

- Monte Carlo Simulation for portfolio optimization.
- Sharpe Ratio Maximization to find the best risk-adjusted return.
- Sector Constraints to limit exposure to specific industries.
- Factor Models (e.g., Fama-French) to enhance risk modeling.
