# COVID-19 Spread Prediction in Pakistan
**Data Processing**
1.	The file we have used is time_series_covid_19_confirmed.csv
2.	First of all we read the file into a dataframe and then restrict the columns till 27/05/2020.
3.	Find the correlations of Pakistan with all the other countries in the dataframes.
4.	Pick top 5 countries.
5.	We extract data of these 5 countries into a separate dataframe.
6.	We display these trends using Sliding Window Average.


**Model Selection and Future Prediction**
1.	The model we are using is an AutoRegression (Exponential Smoothing) model.
2.	Our model accepts inputs in the form of Python lists, so we create country-wise lists of data.
3.	Then we calculate the daily cases from these lists and write them into new lists. 
4.	We input these daily cases lists into our model, and get output in the form of a list, where each next entry is the number of cases predicted for the corresponding date.
The future prediction is done using an AUTOREGRESSION model. It is a simple model with a formula, which provides the next predicted value in a time series. It accepts inputs in the form of lists and outputs a list with predicted values appended to the input list.
The formula for our model is:

![Formula](/images/formula.jpg)

5.	First of all, we predict daily cases for each country from 10/05/2020 to 27/05/2020.
6.	Each new predicted value is used in prediction of the next value.
7.	These predictions are displayed on graphs.
8.	Finally, we predict for 31 days into future from 27/05/2020 to 27/06/2020 using the Pakistan daily cases data, which have been displayed after.

**Findings and Conclusion**
The COVID-19 disease is spreading with a very fast pace in Pakistan, which is quite unfortunate since it is not spreading with such fast speed in other countries.
The data available is very primitive and insufficient to make accurate “COVID-19 daily confirmed cases forecasts”. Our model is an AutoRegressor, which applies exponential smoothing. The forecasted values may not be very accurate, but the RMSE values are quite fair considering the haphazard behavior of the spread of COVID-19.
There are some variables which could have greatly increased the accuracy of our model, had their data been available on our specific set of dates:
1.	Lockdown Status (Yes / No)
2.	Weekend (Yes / No)
3.	Lockdown Enforcement Severity (Scale of 1 to 5)
4.	Markets (Open / Closed)
Furthermore, the data collection might have been done unevenly. For example, the number of cases recorded daily might not have been recorded at the same time every day, which might have resulted in lesser values than actual on some days and more values on others.
Considering all these factors, it can be concluded that the output provided by the AutoRegression model seems realistic and is quite commendable.
