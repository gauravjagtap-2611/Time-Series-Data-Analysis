# Time-Series-Data-Analysis
* * *
## Analysed:
•	Reliance Communication\
•	Indian Foreign Trade (Export)\
•	S&P BSE Sensex\
•	Power Consumption\
•	Foreign Exchange Reserves weekly for Gold\
* * *
## 1.Reliance Communication:

The data consists of closing prices of stock per month starting from 1st January 2000 to 18th December 2020. The data was collected from the website of yahoo finance.
Here we try to model the stock price data using different models, where ARIMA(0,1,0) fits the best.


![image](https://user-images.githubusercontent.com/78009164/107781211-a6121d80-6d6d-11eb-975c-a7661d6e7bd3.png)

## 1.1 Conclusion & Interpretation:
From the above plot we can say that the residuals are stationary in nature. Ljung-Box test also signifies that the residuals are stationary in nature. Thus the best fit for the mo del ARIMA(0,1,0) which is a random walk.  

* * *
       
## 2. S&P BSE Sensex
The data used for the modelling is S&P index of BSE SENSEX from 1st January 2015 to 17th December 2020. This is weekly data consisting of 312 data points. Variables in the data are such as opening and closing sensex for the week, high and low stock sensex for the week and volume. The data was collected from yahoo finance website.\

## 2.1 Modelling Data
I  try to model this using different models like ARIMA(1,1,1) ,SARIMA(0,1,1)*(0,0,1) and SARIMA(0,1,1)*(0,0,1)[52].\
Model_________________________AIC____________BIC\
ARIMA(1,1,1)_______________5036.637_______5047.856 \
SARIMA(0,1,1)*(0,0,1)______5033.007_______5044.226 \
SARIMA(0,1,1)*(0,0,1)[52]__227.2842_______234.4056 

The data on AIC and BIC of each of the models leads us to the conclusion that SARIMA(0,1,1)(0,0,1)[52] is the appropriate fit for the model with seasonal factor and difference factor as 52. We further check the residual of the fitted model are stationary in nature. \
\
I also tried to forecast **volaility Forecasting using GARCH Model.**\

![image](https://user-images.githubusercontent.com/78009164/107784944-030fd280-6d72-11eb-8584-b2e4e33a5474.png)

The black line is the line of squared residuals and the red line is the conditional varian ces. We do observe a typical GARCH pattern where the conditional variances increase s as the squared residual increases. This is due to the volatility. This can be observed b etween 250 and 300

* * *

## 3. Indian Foreign Trade (Export): 

 The data is from April 1990 to July 2020. The variable taken into consideration is export. The data is monthly with April to March as one cycle. \

## 3.1 Exploring Time Series:

Here we can see that there exists trend and seasonality in the data of Exports. 
 
![image](https://user-images.githubusercontent.com/78009164/107842331-6fc5b400-6de8-11eb-9cad-5c4ab6c4b237.png)

## 3.2 Modelling Time Series
AIC and BIC both are minimum for SARIMA(1,1,1)*(0,0,2)[12]. Therefore SARIMA(1,1,1)*(0,0,2)[12] is the best fit for the data. Since there exists seasonal component and it majorly affects the series hence it is the best fit. 


![image](https://user-images.githubusercontent.com/78009164/107842334-7bb17600-6de8-11eb-98a9-34b059111859.png)

The seasonal plot signifies that there exists a seasonal component that affects the model. The plot for the year 2020 shows a strong decrease in exports from February to June. This is obvious as restrictions were imposed by most of the countries due to the pandemic COVID 19. 

* * * 

## 4.Power Consumption: 

The dataset consists of electricity consumption data (Recorded at every hour for 10 days from 28/06/2017 to 11/07/2017) from a high-rise residential building inside the IIT Bombay campus.

![image](https://user-images.githubusercontent.com/78009164/107842496-b831a180-6de9-11eb-9194-faa555d1173e.png)

Here also we try to model our data using different existing Time Series models and came to the conclusion that SARIMA(0,1,1)(0,0,1) is best fit.

* * *

## 5. Foreign Exchange Reserves weekly for Gold: 

The dataset consists of weekly foreign exchange reserves in rupees and US dollars (from 06 April 2001 to 27 November 2020) comprising of 1029 observations

![image](https://user-images.githubusercontent.com/78009164/107842620-be744d80-6dea-11eb-8232-b7b95916fce3.png)

We find that ACF & PACF of the data are not very conclusive, therefore we try to model this data using different models.

The above plot shows the forecasting for the data based on SARIMA model. Prices tend to increase because of the increasing trend. Hence gold prices tend to increase over the years. 
