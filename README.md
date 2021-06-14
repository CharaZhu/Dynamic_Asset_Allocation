# Dynamic Asset Allocation Project

Re-balance portfolio according to a investment strategy at the first trading day of each 2-month holding period (up to 12 re-balances during 2 years): 
given a current portfolio, the market prices on that day, and the estimates of the mean and covariance of the daily returns. These estimates are based on 
the previous two-month data and are updated every second month.
Need to take into account the effect of trading costs.

1. "Buy and hold"  
2. "Equally weighted" (also known as <img src="https://render.githubusercontent.com/render/math?math=\frac{1}{n}">) portfolio  
3. "Minimum variance" portfolio  
4. "Maximum Sharpe ratio" portfolio  
5. "Equal risk contributions" portfolio  
6. "Leveraged equal risk contributions" portfolio  
7. "Robust mean-variance optimization" portfolio 

## Data Files 

Daily_closing_prices.csv: daily closing prices (quoted in US dollars) of 20 stocks from 2019 to 2020

Daily_closing_prices20082009.csv: daily closing prices (quoted in US dollars) of 20 stocks from 2008 to 2009

## Python Implementations: Main.ipynb  

* Implement investment strategies (optimization & re-balance)
* Design rounding procedures (round the number of shares traded to integer values)
* Design validation procedures (Verify cash account are non-negative, have enough budget to re-balance portfolio)
* Result Visualization & Analysis


## Report:
Summarize the key stepes in IPython Notebook, present the results of analysis.

## Background
20 Stocks: MSFT, F, JPM, GOOG, HPQ, C, HOG, VZ, AAPL, IBM, T, CSCO, BAC, INTC, AMD, SNE, NVDA, AMZN, MS, BK

Each transaction has a cost composed of a variable portion only. The variable fee is due to the
difference between the selling and bidding price of a stock, and is 0.5% of the traded volume.

The initial portfolio: IBM = 980 shares, BK = 20000 shares.

The value of the initial portfolio is about one million dollars. The initial cash account is zero USD. The cash account must be nonnegative at all times. 
Cash account does not pay any interest, but cash funds should be used toward stock purchases when portfolio is re-balanced next time.

Note that for buying and selling asset shares, you need to optimize over asset weights. Current
weight of asset i in a portfolio is <img src="http://chart.googleapis.com/chart?cht=tx&chl= w_i = \frac{v_i x_i}{V}">, where
V is the current portfolio value,
<img src="http://chart.googleapis.com/chart?cht=tx&chl= v_i"> is current price of asset i and <img src="http://chart.googleapis.com/chart?cht=tx&chl= x_i">
is the number of units (shares) of asset i in your portfolio.
 
