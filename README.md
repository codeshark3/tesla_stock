### Tesla Stock Price Prediction using Correlation and Random Forest Regression

Stock predictions are a common problem in finance. In this notebook, we will be using the stock price data of the S&P 500 company to predict the future stock prices. We will be using the Correlation to find the most important features and then using Random Forest Regression to predict the future stock prices. This work was done in google colab.


###

Data Collection and Preprocessing

We will be using the data from Yahoo Finance. To get this data we first use beautifulsoup to scape the S&P 500 tickers from wikipedia. We then use the yfinance package to get the stock data. We then use pandas to clean the data.
Data from the separate files are then merged into a single dataframe callded combined_df.
There are multiple data columns in the combined dataset after the merge so we drop all but the first and reorder the columns so that the target is the first column.

### 

Feature Extraction with Colleration

We find the correlations of the features with the target and take the first 10 values which have the strongest absolute correlations.

###

Creating the model
We split the data ino the training and testing set ,train the  and calculate the m2_score and the mean squared error.

### 

Conclusion
We had an r2_score of 0.99 and a mse of 52.76. This shows that our model did well since it had a high r2_score.  More optimizations can be made such as adding cross validation and making changes to the hyperparameters used. Also other models such as LSTMs, Artificial Neural Networks and Multi Layer Perceptrons can be used to seek better results.
