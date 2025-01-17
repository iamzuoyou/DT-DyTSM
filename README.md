# DT-DyTSM: Decision Tree-Based Dynamic Time Series Momentum Strategy

## Overview
This project explores a dynamic Time Series Momentum (TSM) strategy using decision trees to optimize the combination of fast and slow momentum signals based on market volatility. The strategy aims to improve market timing efficiency and reduce drawdowns during periods of high volatility.

## Key Concepts
- **Time Series Momentum (TSM)**: A trend-following strategy that captures upward and downward trends in asset prices by taking long positions during uptrends and short positions during downtrends.
- **Fast and Slow Momentum Signals**: 
  - **Fast Momentum**: Based on a 1-month lookback period.
  - **Slow Momentum**: Based on a 12-month lookback period.
- **Decision Tree Model**: Used to determine the optimal switching mechanism between fast and slow momentum signals based on market volatility.

## Methodology
1. **Data**: Daily return data of the Shanghai Composite Index from December 1990 to December 2024.
2. **Momentum Signals**: Defined as:
   - Long position if the past N-month return is non-negative.
   - Short position if the past N-month return is negative.
3. **Decision Tree Model**: 
   - Trained on 25 years of data (1991-2015) and tested on 9 years of data (2016-2024).
   - Maximum depth of the decision tree is set to 3.
   - The model switches between fast and slow momentum signals based on a volatility threshold of 8.5%.

## Conclusion
- **Performance**: The decision tree-based strategy outperforms both individual fast and slow momentum strategies and a simple 50/50 mix in terms of annualized return, Sharpe ratio, and maximum drawdown.
- **Alpha and Beta Decomposition**: The strategy's excess performance is primarily driven by market timing and volatility timing.

## References
[1] Goulding, C. L., Harvey, C. R., & Mazzoleni, M. G. (2023). Momentum turning points. *Journal of Financial Economics*, 149(3), 378-406.
