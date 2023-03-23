# FinPredict

The purpose of our project was to test whether we could build a profitable trading strategy by using past stock movement data. 

We were successful.

The trading strategy we use is going to be buying when the model predicts that the stocks will go up, and then selling at the end of the day. If the model predicts the stock to go down, we ignore the stock on this day, since Robinhood does not allow inexperienced traders to short stocks. If we took into account shorting, our yield numbers would likely be higher, especially for stocks where the model already had very high yield.

Models built using a Random Forest Regressor had a higher average yield. It was particularly good at building models to predict mining and retail stocks, while Linear Regression was very good at predicting tech and mining stocks but struggled mightily with other industries. K-Nearest Neighbors did well in Retail and Construction, and built profitable models on some car stocks that the other two didn't such as Ford and GM.

It was possible to build a model that was profitable using one of the 3 ML techniques for almost all companies tested: only 8/37 companies we tested had negative yield for all 3. 

Another thing we tried was building indexes by combining the prices of multiple stocks. We found that we were able to make positive returns in our backtest of an index comprised of blue-chip tech stocks, in every time horizon we tried. 

We also experimented with retraining this model every 25 days, in order to take into account the additional data points, and found that this juiced returns even further, from 4.5% YoY to ~25%.

In this repository includes code for data collection from Yahoo Finance's free daily data, some data exploration on distribution and correlations of different stock Close Prices and Daily Changes over time, and code to conduct and measure a backtest of a trading strategy using time-series data, and various ML strategies to predict price.

