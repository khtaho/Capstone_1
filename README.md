## DJIA Stock Predictor
![Header](https://github.com/khtaho/Stock_Predictor/blob/master/candlestick-charts.png "Header")

This model was initially a NLP problem looking at Reddit News Headlines and determining if there was any correlation between the headlines and the DJIA price movement. Below is a summary of the NLP analysis that was done.

The chart above shows the top 50 tokens that appear in 2014 Reddit news headlines.

Another interesting chart is how the frequency of the top 25 tokens appeared over the year. The tokens 'chinese' and crimea' had a large spike.

Then the analysis switched over to a technical analysis to determine features that helped predict the daily closing prices. The regression model attempts to predict the future trend and closing prices of the DJIA in the future.

The data was then converted to TFIDF and we applied several regression models to 2013-2014(2 years) of data.  The above table shows that the best accuracy was at best 57%.

An attempt at fine tuning hyper parameters was also done.  The above table summarizes all the tuning but the highest accuracy was still only 57%.
