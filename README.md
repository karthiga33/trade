Introduction

Objective:

The goal of this analysis was to evaluate and rank Binance trading accounts based on key financial metrics, including ROI, PnL, Sharpe Ratio, Maximum Drawdown (MDD), Win Rate, and Total Positions. The dataset provided historical trade data for multiple Binance accounts over 90 days.

Dataset Overview:

The dataset contains details of trades such as timestamps, assets, side (BUY/SELL), price, quantity, realized profit, and more. The data was used to calculate financial metrics for each account and rank them accordingly.

Methodology

Data Cleaning:

The dataset was cleaned by handling missing values, standardizing column names, and fixing formatting issues, especially with the Trade_History column, which required converting malformed JSON data into a valid format.

Metrics Calculation:

ROI: Calculated by dividing total profit by total investment.

PnL: The sum of realized profits from all trades.

Sharpe Ratio: Calculated as the average return divided by the standard deviation of returns, measuring risk-adjusted performance.

Maximum Drawdown (MDD): The largest peak-to-trough decline in cumulative returns.

Win Rate: The percentage of trades with a positive profit.

Win Positions: The number of profitable trades.

Total Positions: The total number of trades for each account.
Ranking Algorithm:

A weighted scoring system was developed to rank accounts. Metrics such as ROI and PnL were weighted at 30% each, while Sharpe Ratio and Win Rate were weighted at 20% each.
Findings
Top-Performing Accounts: The top 20 accounts were ranked based on the weighted score of the calculated metrics. These accounts demonstrated the best financial performance in terms of ROI, PnL, Sharpe Ratio, and Win Rate.

Key Insights: Accounts with higher ROI and PnL typically had a stronger overall performance, but accounts with a high Sharpe Ratio showed better risk-adjusted returns. Some accounts had a high win rate but lower overall returns, indicating a focus on smaller, consistent profits.
Assumptions

Data Quality: Assumed that the provided trade data was accurate and clean after data cleaning steps.

Missing Data: Rows with missing Trade_History were dropped, assuming this field is critical for calculating metrics.

Static Weights: The weights for each metric in the ranking system (ROI, PnL: 30%, Sharpe Ratio, Win Rate: 20%) were chosen based on a general understanding of the relative importance of each metric in trading performance.
Limitations

Incomplete Data: The dataset might have missing or incomplete entries for some accounts, which could affect the accuracy of the calculated metrics.

Simplified Assumptions: The analysis assumes that the data reflects actual trading conditions without accounting for external market factors or trading strategies beyond the recorded trades.

No Transaction Costs: The analysis did not factor in transaction costs, slippage, or taxes, which could affect the true profitability of each trade.
