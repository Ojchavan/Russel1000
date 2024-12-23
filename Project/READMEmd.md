# Stock Market Analysis Project

## Overview
This project analyzes the risk-return relationships in the Russell 1000 stocks, focusing on predictability patterns in returns, volatility, and various risk metrics. The analysis spans from 1962 through 2024, using daily stock returns and Fama-French factors.

## Project Goals
1. Demonstrate advanced data manipulation and visualization techniques in financial analysis
2. Explore and understand the risk-return tradeoff using multiple risk measures

## Data Sources
- Russell 1000 stock returns (`returns.csv`)
  - Daily returns from 1962 through 2024
  - Sourced from Yahoo Finance
- Fama-French factors (`ff.csv`)
  - Daily factor returns from 1962 through 2024
  - Includes market risk premium and risk-free rate

## Dependencies
- pandas
- numpy
- matplotlib
- seaborn
- yfinance
- pandas_datareader
- requests_cache

## Analysis Components

### Single Stock Analysis
- Return predictability analysis
- Sharpe ratio persistence
- Beta stability analysis
- Relationships between:
  - Volatility and future returns
  - Beta and future returns

### Portfolio Analysis I
- Analysis of 100 random portfolios
- Each portfolio contains 50 equally-weighted stocks
- Daily rebalancing
- Examines:
  - Volatility as a predictor of future returns
  - Beta as a predictor of future returns
- Comparison between single stock and portfolio behaviors

### Portfolio Analysis II
- Monthly volatility-based portfolio formation
- Five portfolios based on previous month's volatility
- Equal weighting with monthly rebalancing
- Minimum 15 daily returns per stock-month
- Analysis of:
  - Return patterns across volatility quintiles
  - Risk-adjusted performance metrics
  - Sharpe ratios across portfolios

## Key Functions
- `mean()`: Calculates annualized mean returns
- `std()`: Calculates annualized standard deviation
- `sharpe()`: Computes Sharpe ratio using risk-free rate
- `beta()`: Calculates CAPM beta
- `stats_all_ann()`: Generates comprehensive annual statistics
- `scatter()`: Creates regression plots with confidence intervals
- `stats_corr()`: Computes correlations with outlier analysis

## Visualization Features
- Scatter plots with regression lines
- Comparative analysis plots
- Portfolio performance visualizations
- Multi-panel comparisons of different metrics

## Usage Notes
- Stock data requires complete returns for analysis periods
- Portfolio analysis uses random sampling for diversification
- Volatility-based portfolios are formed using lagged measures
- All returns and risk metrics are annualized for comparison
