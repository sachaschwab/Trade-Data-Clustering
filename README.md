# Trade-Data-Clustering

## Introduction

Clustering of Stock Price Data using Agglomerative Clustering and GMM
Analysing stock price time series comes with various challenges. One of them is the question whether stock prices behave similarly depending on the sectors and industries they are attributed to.
In this article I investigate whether we can employ unsupervised clustering on the development of stock price over time. I selected two approaches to compare:
Growth Mixture Model (GMM), a probabilistic latent variable growth method that attempts to find a mixture of multidimensional Guassian probability distributions that model the input dataset [6, p. 776].

It differs from basic growth models in that it observes the underlying sub-populations [3]. It is usually employed in health science since it is "considered to be a person-centred method because it is predicated on the assumption that people are the agents that affect the outcomes of interest with predictor variables deemed to be properties of those people" [4]. Thus, one aim of this article is to investigate whether GMM can be employed on non-person related longitudinal data such as stock prices. A motivation for this experiment is that parts of the literature indicate that GMM can be used to represent any data set that can be clustered into multiple Gaussian distributions since the algorithm estimates the parameters of the Gaussian distribution of the different clusters [5].
A concise description of the 'mechanics' of GMM can be found in this Wikipedia article.

The results are less promising than expected. Nonetheless, this article may provide interested readers with useful ideas for their own investigations.
You can access the dataset and the code in this Github repository. 

## Data 
Half-hourly share price data is generated through Financial Modelling Prep's API. I these data in the respository's "data.csv" file, with its
columns: 333 consecutive datapoints covering half-hourly stock price data (usually between 9am and 16pm the same day) ranging from 13 February 2023 to 17 March 2023. The column names are anonymised.
observations (rows): 473 shares along 4 selected industries (Technology' Basic Materials, Industrials, Consumer Cyclical). The stock symbols (tickers) are anonymised.
values: Log returns of the open/close prices (each measured with one time lag).

The sectors the companies belong to are mapped in a seperate csv file "sectors.csv".