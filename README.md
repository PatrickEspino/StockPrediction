# Stock Prediction
This project is for predicting stock prices 10 days into the future

# About
This project utilizes the yfinance library to extract information on stocks in the S&P 500 companies found here https://en.wikipedia.org/wiki/List_of_S%26P_500_companies. These features include open, close, high, low, adjusted close, and volume for each stock.

# Data Visualization
Implemented exploratory data analysis on the chosen stock (GOOGLE)
![ScreenShot](/screenshots/adjclose.PNG)

I also created a heat map to see if there are any correlations between the major tech companies (Meta, Amazon, Netflix, Google, and Apple)
![ScreenShot](/screenshots/heatmap.PNG)

I created a new feature named daily return in order to show where each stock is in terms of return vs risk. Expected return is determined by calculated the mean of daily return and the risk is determined by comparing that mean to the standard deviation of the stock price. All of this is using the Adjusted Close price.
![ScreenShot](/screenshots/risk.PNG)

# Predicting Stock Prices
The first method used for predicting stock prices is by implementing the Monte Carlo Simulation. This model is used to predict outcomes when there are many potential random variables that should be considered i.e. outside circumstances and events that may impact the stock price. I ran 1000 simulations to show how varied each outcome is when predicting the adjusted close price of each stock
![ScreenShot](/screenshots/montecarlo.PNG)

I took the best fit line and compared that to the actual price of Google Stock
![ScreenShot](/screenshots/bestfit.PNG)

Finally, I can use the best fit to predict the next 10 days of the stock
![ScreenShot](/screenshots/montecarloprediction.PNG)

# Implementing LSTM
I built a recurring neural network that is capable of learning long-term dependencies that come with Time Series problems such as stock prices. I used the adam optimizer and calculated loss with mean squared error.
![ScreenShot](/screenshots/lstmcomparison.PNG)

Here is the prediction for the next 10 days
![ScreenShot](/screenshots/lstmprediction.PNG)
