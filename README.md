# Dynamic Asset Allocation Project

The goal of the optimization effort is to create a tool that allows the user to make regular decisions
about re-balancing their portfolio and compare different investment strategies.The basic building block is
a decision made at the first trading day of each 2-month holding period: given a current portfolio,
the market prices on that day, and the estimates of the mean and covariance of the daily returns,
make a decision about what to buy and sell according to a strategy. Need to take into account the
effect of trading costs.

1. "Buy and hold" strategy
2. "Equally weighted" (also known as <img src="https://render.githubusercontent.com/render/math?math=\frac{1}{n}">) portfolio strategy
3. "Minimum variance" portfolio strategy
4. "Maximum Sharpe ratio" portfolio strategy
5. "Equal risk contributions" portfolio strategy
6. "Leveraged equal risk contributions" portfolio strategy
7. "Robust mean-variance optimization" portfolio strategy


Design and implement a rounding procedure, so that you always trade (buy or sell) an integer
number of shares.
Design and implement a validation procedure in your code to test that each of your strategies
is feasible (you have enough budget to re-balance portfolio, you correctly compute transaction
costs, funds in your cash account are non-negative).
There is a le portf optim.py on the course web-page. You are required to complete the
code in the le.

## Data Files 

## Python Implementations



## Background

Trading stocks <img src="http://chart.googleapis.com/chart?cht=tx&chl= S_1, ... S_n">, and the total number of stocks is n = 20. 
At holding period t the expected (daily) return of stock i is 
<img src="http://chart.googleapis.com/chart?cht=tx&chl= \mu^t_i">, the standard deviation of the return is
<img src="http://chart.googleapis.com/chart?cht=tx&chl= \sigma^t_i">. The correlation between the returns
of stocks <a href="https://www.codecogs.com/eqnedit.php?latex=i&space;\neq&space;j" target="_blank"><img src="https://latex.codecogs.com/gif.latex?i&space;\neq&space;j" title="i \neq j" /></a> is <a href="https://www.codecogs.com/eqnedit.php?latex=p^{t}_{ij}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?p^{t}_{ij}" title="p^{t}_{ij}" /></a>. To abbreviate notation we introduce the return vector <img src="http://chart.googleapis.com/chart?cht=tx&chl= \mu^t = {\mu_1^t}
 _i">

