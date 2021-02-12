# Time-Series-Data-Analysis

## Analysed:
•	Reliance Communication\
•	Indian Foreign Trade (Export)\
•	S&P BSE Sensex\
•	Power Consumption\
•	Foreign Exchange Reserves weekly for Gold\

## 1.Reliance Communication:

The data consists of closing prices of stock per month starting from 1st January 2000 to 18th December 2020. The data was collected from the website of yahoo finance.
Here we try to model the stock price data using different models, where ARIMA(0,1,0) fits the best.
![image](https://user-images.githubusercontent.com/78009164/107781211-a6121d80-6d6d-11eb-975c-a7661d6e7bd3.png)
## 1.1 Conclusion & Interpretation:
From the above plot we can say that the residuals are stationary in nature. Ljung-Box test also signifies that the residuals are stationary in nature. Thus the best fit for the mo del ARIMA(0,1,0) which is a random walk.  

       
## S&P BSE Sensex
The data used for the modelling is S&P index of BSE SENSEX from 1st January 2015 to 17th December 2020. This is weekly data consisting of 312 data points. Variables in the data are such as opening and closing sensex for the week, high and low stock sensex for the week and volume. The data was collected from yahoo finance website.\

I  try to model this using different models like ARIMA(1,1,1) ,SARIMA(0,1,1)*(0,0,1) and SARIMA(0,1,1)*(0,0,1)[52].\
**Model 	                    AIC      	BIC **\
ARIMA(1,1,1)         	5036.637 	5047.856 \
SARIMA(0,1,1)*(0,0,1) 	5033.007 	5044.226 \
SARIMA(0,1,1)*(0,0,1)[52] 	227.2842 	234.4056 \

The data on AIC and BIC of each of the models leads us to the conclusion that SARIMA(0,1,1)(0,0,1)[52] is the appropriate fit for the model with seasonal factor and difference factor as 52. We further check the residual of the fitted model are stationary in nature. \
\
I also tried to forecast **volaility Forecasting using GARCH Model.**\
The black line is the line of squared residuals and the red line is the conditional varian ces. We do observe a typical GARCH pattern where the conditional variances increase s as the squared residual increases. This is due to the volatility. This can be observed b etween 250 and 300
