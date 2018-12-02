
## 4501 Project: Python Applied in Stock Investing Strategies

**Group name:** Sure-we-can

**Group Members:** Wenda Guo, Qihan Liang, Qinxin Wu, Xia Chu

**Backgrounds:**
With the development of Quantitative Trading, python has already transferred lots of  mathematical models into practical applications with more profits. It plays an important role in financial industry since it helps us to make decisions more efficiently and accurately in this rapidly changing world. However, capital market can always be influenced by many factors. Especially, the stock fluctuates in a way that is hard to detect. In order to catch the opportunity and maximize the profit, we need to apply different strategies to find better a prediction for the stock market.

**Our goal:**
We implemented three quantitative trading strategies using python and evaluated their performance by comparing their rate of returns for a period of 2 years. The first strategy is the theoretical analysis of classic theory -- Markowitz Model and the later two strategies are the ones popular to use in the field now. The dataset used for our project includeds daily close price and volume of the day for the most active 263 stocks from Yahho Finance for the past two-year time period from 2016-11-21 to 2018-11-20.


---
**Strategy 1: Markowitz Model(theoratical analysis)**

Choosing stock portfolio with Markowitz mean-variance model, which is based on the expected returns (mean) and the standard deviation (variance) of different portfolios in a time period. Generating a large number of random portfolios from the existed stock pool, divide the stock pool into three sets. Picking up the portofolio using a package to find the optimal portofolio with highest rate of return and the proportion of the choosing stocks in the pool respectively. Later using these three optimal portfolios to generate a new optimal solution, which is the result we want. In general, we modified the Markowitz model with greedy algorithm, which reachs a satisfying outcome. And we take it as the base in comparison.
1. Use log function to generate the return of each stock	
2.	Generate 1000 random portfolio to make simulations
3.	Divide stock pool into 3 parts and figure out the optimal solution in each set
4. Use Markowitz model to calculate the mean rate of return and volatility of each portfolio
5. Utilizing three optimal solutions to get an optimal solution for the original problem, which is greedy algorithm
6. Draw graphs to clarify the results and make it as the base for later comparison


---
**Strategy 2: Alpaca Model**

The most common strategy for investment is always choosing the stock with the highest yield, and make quick changes to the allocation based on the changes in the combination of stocks. The alpaca model chooses stock portfolio based on N stocks with the highest yield, and make changes to allocation based on the changes in the list of stocks that belongs to the top N number of highest yields. In a simple Alpaca Model, we assume that the asset used to buy each stock is equally distributed.

*Procedures*
1. Set N number of stocks to put in portfolio and the total initial asset wanted to use. In our specific model, we chose N = 30.
2. Calculate yield by changes in market capitalization and choose top 30 stocks with the highest yield to make our stock combination.
3. Buy all 30 stocks on the first day and make changes on every trading day by comparing the combinations from 2 days:
  * Sell the stock if it was in the last trading day's combination but not in today's. 
  * Buy the stock if it is in today's stock combination not the last trading day's (number of shares to buy is decided by the total asset available and the price of the stock that day).
4. Repeat step3 for every day included in our dataset to perform stock reallocation on every trading day and calculate the change in rate of return for time period from 2016-11-21 to 2018-11-20.


---
**Strategy 3: Small-Cap Model**

The most popular short_term strategy is choosing stocks with the smallest market capitalization as they have more chances to increase in values. Choosing stock portfolio based on N stocks with the smallest market capitalization, and make changes to allocation based on the changes in the list of stocks that belongs to the top N number of smallest market capitalization. In a simple Small-Cap Investing model, we assume that the asset used to buy each stock is equally distributed. In our specific model, we chose N = 30 as the number of stocks will be considered for allocation every time we want to perform a change (the next stock exchange day).

*Procedures*
1. Set the number of stocks to put in portfolio, N = 30 and the total initial asset wanted to use.
2. Find the first 30 number of stocks with the smallest market capitalization of the day to form our initial combination. 
3. Compare with top 30 smallest the next day to determine what stocks and how many shares to sell or buy:
  * Sell the stock if the market capitalization of the current holding stock is not small enough anymore (not in the new combination of 30 stocks)
  * Evenly distribute available asset to buy new stocks (from the current combination of 30 stocks with the smallest market capitalization).
4. Repeat step3 for every trading day included in our dataset to perform stock reallocation on every stock exchange day and calculate the change in rate of return for time period from 2016-11-21 to 2018-11-20.


---
**Run Instruction**

•	What do I need to type to get your program to do its thing

1. cloning the repo: 
2. To use fixed Yahoo_Install Fix_Yahho_Finance package: type `pip install fix_yahoo_finance --upgrade --no-cache-dir` at terminal (We got our data from Yahoo Finance. However, the portal might not be stable over the time. In order to keep our data consistent throughout the usage, we saved the data into a csv called 'Data.csv' for all later usage. 
3. 


---
**Expected Output**

![Image](https://github.com/Nancyliangqh/Sure-we-can/blob/master/Markowitz.png)

![Image](https://github.com/Nancyliangqh/Sure-we-can/blob/master/Alpaca.png)

![Image](https://github.com/Nancyliangqh/Sure-we-can/blob/master/SmallCap.png)

As yield curves from three strategies showed, Markowitz Model gave the highest yield and Alpaca Model gave the lowest yield. In fact, Markowitz Model is a theoretical analysis that only focuses on the systematic risk of the entire stock market yet ignores corporate factors that may affect the stock prices. Thus, we got an ideal result based on statistics and probabilities, but it does not make much sense in the real market. Then, we checked the yield generated from Alpaca Model, the most common strategy for investment. As the stock prices fluctuates frequently every day, the highest stocks combination picked also changes greatly compare to the Markowitz Model. Due to the frequent changes, we cannot share the value increments for one specific stock during a time period, thus led to a very low yield in return. Finally, we chose a more popular model Small-Cap Model to determine the stocks to hold based on small capitalization as they have more potential to increase in values throughout the time. Capitalization will be stable during a time period, so our everyday-portfolio will not change greatly and thus share more returns through holding a stock for certain days. Looking at at the yield from Small-Cap Model, it gives us a better yield then Alpaca Model and we might be able to use this strategy for investment in the future.


---
**Reference:**

1. Wiecki, T. (2015, March 9). The Efficient Frontier: Markowitz portfolio optimization in Python. Retrieved from https://blog.quantopian.com/markowitz-portfolio-optimization-2/

2. Brenyah, B. (2017, October 21). Markowitz's Efficient Frontier in Python [Part 1/2]. Retrieved from https://medium.com/python-data/effient-frontier-in-python-34b0c3043314
