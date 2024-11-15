# group1_factor_backtesting

Goal:  
Build a single-factor stock selection strategy.

Steps:
Obtain A-share data 
The daily data for A-shares are from the Tushare financial API, covering the period from January 1, 2014, to December 1, 2023.

Factor identification
The factor we focus on is Earnings-to-Price ratio (EP), which is the inverse of the P/E ratio (1/PE_TTM).

Data preprocessing
Delete extreme values, Standardization and Industry market value Zero-centered.
Reasons: The distribution of factor may vary significantly across different industries and market values; If multiple factors are used, this ensures comparability between factors.

Stock ranking and grouping
Stocks are ranked by their factor values and divided into decile-based groups.

Portfolio Construction
The bottom 30 stocks are selected within each group.

Rebalancing
On the designated rebalancing dates, recalculate factor rankings and adjust the portfolio. The first trading day of each month is chosen as the rebalancing date.

Performance Monitoring
Track the portfolio's returns over time and plot a benchmark return graph (compared to the CSI 500 return rate).
Calculate the factor Information Coefficient (IC) value, Sharpe ratio and annual return.

tushare接口导入部分可能因为接口过期等原因跑不了。但是数据我们已经下载到了本地，可以直接在导入数据部分跑
