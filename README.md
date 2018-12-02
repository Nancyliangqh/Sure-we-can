
## Topic: Python Applied in Quantitative Trading

Project for 4501

Group name: Sure-we-can

Group Members: Qihan Liang, Qinxin Wu, Wenda Guo, Xia Chu

**Backgrounds:**
With the development of Quantitative Trading, python has already transferred lots of  mathematical models into practical applications with more profits. It plays an important role in financial industry since it helps us to make decisions more efficiently and accurately in this rapidly changing world. However, capital market can always be influenced by many factors. Especially, the stock fluctuates in a way that is hard to detect. In order to catch the opportunity and maximize the profit, we need to apply different strategies to find better a prediction for the stock market.

**Our goal:**
We are planning to implement several quantitative trading strategies through python and evaluate their performance using financial data, some of which are the classic ones and some of which are popular in the fields now. The operational mechanism of those strategies is exactly the function we would like to realize in our coding----when, what, and how much to trade given a certain circumstance in the market. To do so, we will scrape data from web to test the strategies’ efficiency and their precision of forecasting and yields.


•	A description of what has been implemented

1. We choose three methods for stock trading and make comparison among them. Two of those are trendy quantitative strategies       that are often used in daily life. And one is classic method that based on theoratical analysis.
2. Our investing strategies are mainly designed for short-term (daily, T+1) stock allocation. We got a set of daily stock data from Yahoo Finance to use to evaluate our stock investing strategies. The data describes daily: open price, close price, highest price, lowest price, volume of the day for a total of the most active 263 stocks for the time period from 2016-11-20 to 2018-11-20. 


**Stratefy 1: Markowitz Model Investing(theoratical analysis)**

Choosing stock portfolio based on Markowitz mean-variance model, which is based on the expected returns (mean) and the standard deviation (variance) of different portfolios in a time period. Generating a large number of random portfolios from the existed stock pool, picking up the portofolio with high sharpe ratio(return per risk). Also, we use a package to find the optimal portofolio with highest rate of return and the proportion of the choosing stocks in the pool.



•	Installation instructions (if any besides cloning the repo)
•	Python packages should be listed appropriately in requirements.txt

1.	Numpy
2.	Pandas
3.	scipy
4. matplotlib
5. fix_yahoo_finance


•	Run instructions
•	What do I need to type to get your program to do its thing

1.	To get data from Yahoo Finance:
a.	Install Fix_Yahho_Finance using:
b.	pip….
2.	To apply strategies and get the portfolio for stocks choices:
a.	Code need to run
3.	 Compare the rate of return for different strategies
a.	Code need to run


**Strategy 2: High-yield Investing**

The most common strategy for investment is always choosing the stock with the highest yield, and make quick changes to the allocation based on the changes in the list of stocks. In the High-yield Investing model, we get top 30 stocks whoes yield is high every day, and then decide to sell or keep former stocks or buy new ones in the list for acquiruing more profits with the portfolio.

*Procedures*
1.input the start_date you want to enter the market, the original asset you want invest.
2.calculate yield by changes in market capitalization and choose top 30 stocks.
3.buy all 30 stocks on the first day and make changes every day by comparing today's list with the last trading day's list
  sell:  all stocks appeared in the last trading day's list not today's.
  keep: stocks appeard in the both lists
  buy:  N stocks appear in the today'list not the last trading day's( N is decided by the total cash owned  and the price that    day).
4.calculate the total yield for comparing with other strategies.



**Strategy 3: Small-Cap Investing**

The most popular short_term strategy is choosing stocks with the smallest market capitalization as they have more chances to increase in values. Choosing stock portfolio based on N stocks with the smallest market capitalization, and make changes to your allocation based on the changes in the list of stocks that belongs to the N number of smallest market capitalization. In a simple Small-Cap Investing model, we assume that the asset used to buy each stock is equally distributed. In our specific model, we chose N = 30 as the number of stocks will be considered for allocation every time we want to perform a change.

*Procedures*
1. Set the number of stocks want to trade, N.
2. Find the first N number of stocks with the smallest market capitalization.
3. Sell the stock if the price of the current stock holding is not small enough anymore (no in the list of N stocks)
4. Buy the new stocks from the current list of N stocks with the smallest market capitalization.


