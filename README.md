# Time-Series-Homework
## Regression Analysis.ipynb
In this notebook, you will build a SKLearn linear regression model to predict Yen futures ("settle") returns with lagged Yen futures returns.

Overall, our model has a root mean squared error of ~0.415 on the out-of-sample data, and ~0596% on the in-sample data. This means that the model actually performs slightly better on data that it hasn't seen before.

Generally, however(through not always), we should expect a higher error rate on the out-of-sample data than the in-sample data, since the model is specifically trained to predict the in-sample data as well as it can. It's possible that if we contined adding additional data as time goes on, out-of-sample performance may not continue to be as good (so out-of-sample RMSE may rise.)

## Time Series Analysis.ipynb

In this notebook, you will load historical Dollar-Yen exchange rate futures data and apply time series analysis and modeling to determine whether there is any predictable behavior.

Based on the model evaluation, would you feel confident in using these models for trading?

Based on our time series analysis, it would make sense to buy the yen now, with anticipation that it will rise further over the next five days. However, risk(up or down volatile movements) is also forecast to rise, so even if we're right there might be some days in the interim where we see larger than usual swings in the price.

Overall, our model for the forecasting volatility looks reasonably solid. However, our models for prediciting future yen returns (ARMA) seems like they could use some improvement before we actually start using them to make financial bets. This is because none of the features in the model (i.e., the lags) were significant, as all had p-values well above 0.05