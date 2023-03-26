# Clustering of Stock Price Data using Agglomerative Clustering and GMM

Analysing stock price time series comes with various challenges. One of them is the question of whether stock prices behave similarly depending on the economic sectors and industries.
In this article I investigate whether we can employ unsupervised clustering on the development of stock price over time.

[See the code notebook (jupyter) for a report and python code.](https://github.com/sachaschwab/Trade-Data-Clustering/blob/main/code.ipynb)

The results using GMM are less promising than expected. Nonetheless, this article may provide interested readers with useful ideas for their own investigations.

## Data 

[The data are available in the data.csv file in this repository](https://github.com/sachaschwab/Trade-Data-Clustering/blob/main/data.csv)

Half-hourly share price data is generated through Financial Modelling Prep's API. I these data in the respository's "data.csv" file, with its

- columns: 333 consecutive datapoints covering half-hourly stock price data (usually between 9am and 16pm the same day) ranging from 13 February 2023 to 17 March 2023. The column names are anonymised.

- observations (rows): 473 shares along 4 selected industries (Technology' Basic Materials, Industrials, Consumer Cyclical). The stock symbols (tickers) are anonymised.

- values: Log returns of the open/close prices (each measured with one time lag).

### Requirements:
- Python 3.7
- Jupyter Notebook
- Standard Python data science libraries