# Sure-we-can
Project for 4501
Topic: Python Applied in Quantitative Trading
Group Members: Wenda Guo, Xia Chu, Qinxin Wu, Qihan Liang

Backgrounds:
With the development of Quantitative Trading, python has already transferred lots of  mathematical models into practical applications with more profits. It plays an important role in financial industry since it helps us to make decisions more efficiently and accurately in this rapidly changing world. However, capital market can always be influenced by many factors. Especially, the stock fluctuates in a way that is hard to detect. In order to catch the opportunity and maximize the profit, we need to apply different strategies to find better a prediction for the stock market.

Our goal:
We are planning to implement several classical mathematics models into practice through python and evaluate their performance using financial data.
We will choose some quantitative trading strategies, some of which are the latest ones and some of which are popular in the fields now. The operational mechanism of those strategies is exactly the function we would like to realize in our coding----when, what, and how much to trade given a certain circumstance in the market. To do so, we will scrape data from web to test the strategies’ efficiency and their precision of forecasting and yields.


•	A description of what has been implemented

1.	We got a set of daily stock data from Yahoo Finance to use to build our stock investing strategies. The data describes daily: open price, close price, highest price, lowest price, volume of the day for a total of X stocks for the time period from 2017-11-20 to 2018-11-19.
2.	Our investing strategies are mainly designed for short-term (daily, T+1) stock allocation.
3. We choose three methods for stock trading and make comparison among them. Two of those are trendy quantitative strategies that are often used in daily life. And one is classic method that based on theoratical analysis.


Strategy 1: Small-Cap Investing
Choosing stock portfolio based on N stocks with the smallest market capitalization, and make changes to your allocation based on the changes in the list of stocks that belongs to the N number of smallest market capitalization. In a simple Small-Cap Investing model, we assume that the asset used to buy each stock is equally distributed.
In our specific model, we chose N = 30 as the number of stocks will be considered for allocation every time we want to perform a change.

Stratefy 3: Markowitz Model Investing
Choosing stock portfolio based on Markowitz mean-variance model, which is based on the expected returns (mean) and the standard deviation (variance) of different portfolios. Generating a large number of random portfolio from the existed stock pool, 




•	Installation instructions (if any besides cloning the repo)
•	Python packages should be listed appropriately in requirements.txt

1.	Numpy
2.	Pandas
3.	


•	Run instructions
•	What do I need to type to get your program to do its thing

1.	To get data from Yahoo Finance:
a.	Install Fix_Yahho_Finance using:
b.	pip….
2.	To apply strategies and get the portfolio for stocks choices:
a.	Code need to run
3.	 Compare the rate of return for different strategies
a.	Code need to run
