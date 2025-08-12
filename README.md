# MSDS451_Assignment3  

Automated Algorithmic Trading on XOM (2010–2025)

This project implements an automated trading system for ExxonMobil (XOM) using multi-level predicted returns, incorporating Random Forest, LSTM, and options-based strategies. The focus is on automated trade execution, rather than predictive modeling alone, with performance evaluated via backtesting.

## Contents
- `MSDS451_A3.ipynb`: Full notebook with code, analysis, and plots  
- `MSDS451_A3.html`: HTML export of the notebook  
- `MSDS_451_A3.pdf`: Final research report (LaTeX-formatted)

## Summary of Strategies

| Strategy                   | Cumulative Return | Annualized Return | Volatility | Sharpe | Max Drawdown |
|---------------------------|------------------:|------------------:|-----------:|------:|-------------:|
| Random Forest             | 38.5285×          | 27.79%            | 13.84%     | 1.84  | -33.78%      |
| LSTM                      | 0.8993×           | -0.71%            | 9.75%      | -0.02 | -36.06%      |
| Options/Short (Realistic) | 17,355,139,155×| 387.10%           | 48.83%     | 3.49  | -34.76%      |
| Options/Short (Decay)     | 0.0032×           | -32.03%           | 8.11%      | -4.72 | -99.68%      |
| Buy & Hold                | 2.8282×           | 7.23%             | 25.01%     | 0.40  | -62.40%      |

> The extremely high Cumulative Return for the Options/Short (Realistic) strategy reflects optimistic assumptions (e.g., no slippage, margin constraints, or borrow costs) and is not realistic in practice.

## How to Run
1. Open `MSDS451_A3.ipynb` in Google Colab or a local Jupyter environment
2. Run all cells sequentially from top to bottom
3. Outputs (tables and plots) will be generated inline
4. No external datasets are required — the notebook downloads XOM price data directly from Yahoo Finance via `yfinance`

## Research Report
The report (PDF) includes:
- Problem description
- Data preparation and feature engineering
- Model training (Random Forest, LSTM)
- Options-based strategies (realistic and premium decay)
- Backtesting methodology
- Performance metrics and analysis
- Conclusions, limitations, and future work

## AI Usage Disclosure
ChatGPT was used to:
- Debug Python code for backtesting and options strategies
- Suggest volatility filters
- Edit the LaTeX research report

## Submission URL
GitHub Repository (cloneable): https://github.com/bcaldwell21/MSDS451_Assignment3.git
