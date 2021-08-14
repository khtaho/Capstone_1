## DJIA Stock Predictor
![Header](https://github.com/khtaho/Stock_Predictor/blob/master/candlestick-charts.png "Header")

This model was initially a NLP problem looking at Reddit News Headlines and determining if there was any correlation between the headlines and the DJIA price movement. Let's start looking at the NLP analysis that was done.

![Header](https://github.com/khtaho/Stock_Predictor/blob/master/newplot(1).png "Header")

The chart above shows the top 50 tokens that appear in 2014 Reddit news headlines.



![Header](https://github.com/khtaho/Stock_Predictor/blob/master/plot1.png "Header")

The chart above shows the frequency of the top 25 tokens appeared for the year 2014. The tokens 'chinese' and crimea' had a large spike.
<br/>
<br/>

![Header](https://github.com/khtaho/Stock_Predictor/blob/master/accuracy.png "Header")

The data was then converted to TFIDF and we applied several regression models to 2013-2014(2 years) of data.  The above table shows that the best accuracy was at best 57%.

<br/>

![Header](https://github.com/khtaho/Stock_Predictor/blob/master/grid%20search.jpg "Header")


An attempt at fine tuning using GridSearchCV on the hyper parameters was also done.  The above table summarizes all the tuning but the highest accuracy was still only 57%.
<br/>
<br/>
With this learning we can conclude that NLP analysis is not very fruitful. It maybe useful to use different news headlines from another source than Reddit because the Reddit news headlines are global headlines and the DJIA is a conglomerate of just American companies. As we know what does not work so let's pivot over to a technical analysis to determine features that helped predict the daily closing prices. 



![Header](https://github.com/khtaho/Stock_Predictor/blob/master/stock%20features1a.jpg "Header")


![Header](https://github.com/khtaho/Stock_Predictor/blob/master/stock%20features2.png "Header")

The above table details the features that were used in the regression model.<br/>


![Header](https://github.com/khtaho/Stock_Predictor/blob/master/stock%20regression.png "Header")

The training data was from 8-8-2008 to 12-31-2014 and the test data was from 1-2-2015 to 7-1-2016. Above is the predicted stock close price for the test data.  There were 4 regression methods used, Stochastic Gradient Descent, Random Forest, Support Vector and Neural Network.The Neural Network wasn't very accurate so it was not shown in the above chart. We can notice that the regressor match the actuals(blue line) to a good degree.

![Header](https://github.com/khtaho/Stock_Predictor/blob/master/5%20day%20stock%20forecast.png "Header")

Zooming into the data, we look at 5 days to see how accurate the regressors are.<br/>
<br/>

![Header](https://github.com/khtaho/Stock_Predictor/blob/master/error%20chart.png "Header")

Above are various measures of the error of the regressors compared to Actuals. The Entire Forecast is comparing all the data from 2015 to 2016. On the 5 day forecast on the right the Random Forest and Support Vector offer the smallest amount of error but if we look at the entire forecast, Support Vector has the smallest error and therefore the best regressor.  The  modle is not precise but the model can predict the trend of the close price in the long term which has a usability.
