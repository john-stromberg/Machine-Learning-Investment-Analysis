# Machine-Learning-Investment-Analysis

Proposal: 
Predicting the price of stock using historical price data, with python, scikit-learn, keras/tensorflow.

Disclaimer: Predicting stock prices accurately is very challenging as price is impacted by many different variables and potentially random occurences outside of company financial data. Creating reliable models to make profitable investment decisions will require a lot more work.

Interests: Using machine learning and coding generally applied to investing and trading. Good topic to get my feet wet with machine learning with a large amount of data easily and readily available, literature on the subject, and many examples. 

Data Sources: quandl, yahoo
Stocks: Google, Apple, Facebook
Libraries: pandas, matplotlib, numpy, sklearn, keras, quandl

Machine Learning Models: 
-Linear Regression 
-Support Vector Regression -  using three different kernals: 	Linear, Poly, RBF (radial basis function)
-Long Short Term Memory (LSTM) - Artificial Recurrent Neural 	Network 

1: Predicting open price for Google stock (GOOG) on final day on month (30) using data from previous days in month using three support vector regression models and linear regression model, comparing the four outputs.
	- independent variable (X): dates
	- dependent variable (y): open price
create, fit, and plot the models
show plot and predicted price for day 30 for each model

SVR RBF appears to be most succesful modeling the data and predicting day 30 opening price. Closest to actual day 30 open price 


2: Forecasting adjusted closing price for Facebook stock (FB) for 30 days using linear regression and support vector regression (rbf) models with data retreived from quandl, which include May 2012-March 2018, so about 6 years
	- independent variable (X): actual Adj. Closing price
	- dependent variable (y): prediction Adj. Closing price

Split data into training and testing data with 80% training and 20% testing

Create and train the support vector regression model
Test and score the model with the coefficient of determination being the R Squared Value. 
	-SVR RBF score: 0.9833580060203231

Create and train the linear regression model
Test and score the model with the coefficient of determination being the R Squared Value. 
	-Lin Reg score: 0.9831413979917554

Use a variable for last 30 days of Adj Close price to forecast 30 days of predicted Adj. closing price with each model


3: Use an artificial recurrent neural network called Long Short Term Memory (LSTM)to predict closing stock price of Apple using past 60 days price data. 
Train/test split to 80% train and 20% split
Preprocess the data using MinMaxScalar to fit data into LSTM model
Create training data for independent (X) and dependent variables (y) using increments of the past 60 days to predict 61st day.
X_train contains past 60 values 
y_train contains 61st value

reshape tarni data into three dimentional to fit into LSTM network(n of samples, n of time steps, n of features)

Build LSTM model:
-add LSTM layers with 50 neurons
-add Dense layers, one with 25 neurons and one with 1 neuron

train the model, test the model, calculate root mean squared error (RMSE)= 0.24183494567871094
low = better fit

make predictions, validate predictions with actual price data
plot


Where to take the project: 
add another neaural network model, add stock price technical indicators to the equation and use machine learning to determine which is the most successful at predicting up/down price movement 
decision tree, random forest. Add interative visualization to illustrate multiple models 
 