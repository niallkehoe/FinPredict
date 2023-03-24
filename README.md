In this project, we aimed to test whether we could develop a profitable trading strategy by analyzing past stock movement data. Fortunately, we were able to succeed in this endeavor.

Our trading strategy involved buying stocks when our model predicted that the stock price would rise, and then selling them at the end of the day. If the model predicted that the stock price would decrease, we ignored it for the day, as our brokerage (Robinhood) does not allow inexperienced traders like us to short stocks. If we had considered shorting, our yield numbers might have been higher, particularly for stocks where the model already had very high yield.

We used three different machine learning techniques, including Random Forest Regressor, Linear Regression, and K-Nearest Neighbors, to build models for different stocks of various industries. Random Forest Regressor was particularly good at predicting mining and retail stocks, while Linear Regression was excellent at predicting tech and mining stocks but struggled with other industries. K-Nearest Neighbors performed well in Retail and Construction, and it also built profitable models on some car stocks that the other two techniques didn't, such as Ford and GM. We were able to develop a profitable model using one of the three machine learning techniques for almost all companies we tested. Only 8 out of 37 companies we tested had negative yields for all three techniques.

We also attempted to build indexes by combining the prices of multiple stocks. We found that we were able to generate positive returns in our backtest of an index comprised of blue-chip tech stocks across all the time horizons we tried.

We also experimented with retraining our model every 25 days to account for additional data points. This approach boosted our returns even further, from 4.5% YoY to approximately 25%.

In our project, we coded the data collection process from Yahoo Finance's free daily data, conducted data exploration on distribution and correlations of different stock Close Prices and Daily Changes over time, and built a backtesting code to measure the effectiveness of our trading strategy using time-series data and various ML strategies.
