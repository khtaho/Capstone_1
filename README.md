## DJIA Stock Predictor
![Header](https://github.com/khtaho/Stock_Predictor/blob/master/candlestick-charts.png "Header")

This model was initially a NLP problem looking at Reddit News Headlines and determining if there was any correlation between the headlines and the DJIA price movement. Let's start looking at the NLP analysis that was done.

![Header](https://github.com/khtaho/Stock_Predictor/blob/master/newplot(1).png "Header")

The chart above shows the top 50 tokens that appear in 2014 Reddit news headlines.



![Header](https://github.com/khtaho/Stock_Predictor/blob/master/plot1.png "Header")

Another interesting chart is how the frequency of the top 25 tokens appeared over the year. The tokens 'chinese' and crimea' had a large spike.



![Header](https://github.com/khtaho/Stock_Predictor/blob/master/accuracy.png "Header")

The data was then converted to TFIDF and we applied several regression models to 2013-2014(2 years) of data.  The above table shows that the best accuracy was at best 57%.



![Header](https://github.com/khtaho/Stock_Predictor/blob/master/grid%20search.jpg "Header")


An attempt at fine tuning using GridSearchCV on the hyper parameters was also done.  The above table summarizes all the tuning but the highest accuracy was still only 57%.


With this learning we can conclude that NLP analysis is not very fruitful. It maybe useful to use different news headlines from another source than Reddit because the Reddit news headlines are global headlines and the DJIA is a conglomerate of just American companies. As we know what does not work so let's pivot over to a technical analysis to determine features that helped predict the daily closing prices. 



![Header](https://github.com/khtaho/Stock_Predictor/blob/master/stock%20features1a.jpg "Header")


![Header](https://github.com/khtaho/Stock_Predictor/blob/master/stock%20features2.png "Header")

The above table details the features that were used in the regression model.


![Header](https://github.com/khtaho/Stock_Predictor/blob/master/stock%20regression.png "Header")

![Header](https://github.com/khtaho/Stock_Predictor/blob/master/5%20day%20stock%20forecast.png "Header")


![Header](https://github.com/khtaho/Stock_Predictor/blob/master/error%20chart.png "Header")

The regression model attempts to predict the future trend and closing prices of the DJIA in the future. The training data was from 8-8-2008 to 12-31-2014 and the test data was from 1-2-2015 to 7-1-2016.
