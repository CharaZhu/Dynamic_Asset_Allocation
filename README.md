# Dynamic Asset Allocation Project

Implement and compare computational investment strategies. 

Re-balance portfolio according to a strategy at the first trading day of each 2-month holding period 
(up to 12 re-balances during 2 years): given a current portfolio,
the market prices on that day, and the estimates of the mean and covariance of the daily returns.
Need to take into account the effect of trading costs.
 
 
1. "Buy and hold"  
2. "Equally weighted" (also known as <img src="https://render.githubusercontent.com/render/math?math=\frac{1}{n}">) portfolio  
3. "Minimum variance" portfolio  
4. "Maximum Sharpe ratio" portfolio  
5. "Equal risk contributions" portfolio  
6. "Leveraged equal risk contributions" portfolio  
7. "Robust mean-variance optimization" portfolio 


## Data Files 

Daily_closing_prices.csv: daily closing prices of 20 stocks from 2019 to 2020

Daily_closing_prices20082009.csv: daily closing prices of 20 stocks from 2008 to 2009

## Python Implementations


* Design rounding procedures (trade an integer number of shares)
* Design validation procedures (have enough budget to re-balance portfolio, you correctly compute transaction
costs, funds in your cash account are non-negative).
There is a le portf optim.py on the course web-page. You are required to complete the
code in the le.


## Background

Trading stocks <img src="http://chart.googleapis.com/chart?cht=tx&chl= S_1, ... S_n">, and the total number of stocks is n = 20. 
At holding period t the expected (daily) return of stock i is 
<img src="http://chart.googleapis.com/chart?cht=tx&chl= \mu^t_i">, the standard deviation of the return is
<img src="http://chart.googleapis.com/chart?cht=tx&chl= \sigma^t_i">. The correlation between the returns
of stocks <a href="https://www.codecogs.com/eqnedit.php?latex=i&space;\neq&space;j" target="_blank"><img src="https://latex.codecogs.com/gif.latex?i&space;\neq&space;j" title="i \neq j" /></a> is <a href="https://www.codecogs.com/eqnedit.php?latex=p^{t}_{ij}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?p^{t}_{ij}" title="p^{t}_{ij}" /></a>. To abbreviate notation we introduce the return vector <img src="http://chart.googleapis.com/chart?cht=tx&chl= \mu^t = {\mu_1^t}
 _i">

