# Cyrptocurrency
Cryptocurrencies
## Analysis Overview
The purpose of this project is to use unsupervised machine learning to analyze a database of cryptocurrencies and create a report including what cryptocurrencies are traded in the market and how they could grouped by (according to their features).  This classification system will be used for new investments.  Since there is no known output for this classification, I will use unsupervised learning.
This classification report could be used by an investment bank to propose a new cryptocurrency investment portfolio to its customers.

# We use the following methods for the analysis:
- **Deliverable 1:** Preprocessing the database for PCA,
- **Deliverable 2:** Reducing the data dimension using PCA (Principal Component Analysis),
- **Deliverable 3:** Clustering cryptocurrencies using K-Means,
- **Deliverable 4:** Visualizing classification results with 2D and 3D scatter plots.

# Resources
•	Data Source: crypto_data.csv, CryptoCompare
•	Software: Python 3.8.5, Anaconda Navigator 1.9.12, Conda 4.9.2, Jupyter Notebook 6.3.0

# Results
Following the preprocessing and cleaning phase we have a total of 532 tradable cryptocurrencies.

# Clustering Cryptocurrencies using K-Means - Elbow Curve
As we don't know what the output of the analysis would be so we are using unsupervised machine learning to identify clusters of the cryptocurrencies.

## K-Means Elbow Curve
![image alt <](/Images/bokeh_plot1_elbow.png)<br />
We produced the elbow curve below using the K-Means method iterating on k values from 1 to 10.

The best k value appears to be 4 so we would conclude on an output of 4 clusters to categorize the cryptocurrencies.


# Visualizing Cryptocurrencies Results
## 3D-Scatter plot with clusters
![image alt <](/Images/scatter.png)<br />
This 3-D scatter plot was obtained using the PCA algorithm to reduce the cryptocurrencies dimensions to three principal components.


## 2D-Scatter plot with clusters
![image alt <](/Images/scatter_by_class.png)<br />
This 2-D scatter plot was obtained using the PCA algorithm to reduce the cryptocurrencies dimensions to two principal components.

Both these scatter plots show the distribution and the four clusters of cryptocurrencies.
We can identify the outliers like the unique cryptocurrency in the class #2.


## Tradable Cryptocurrencies Table
![image alt <](/Images/tradable_currencies.PNG)<br />


A more detailed look at the clusters show:
- Most of the cryptocurrencies are part of Class #0 and #1.

![image alt <](/Images/class_2_BTT.PNG)<br />
- **Class 0:** are the typical “well-know” tradable currencies, like Bitcoin (BTC #1), Ethereum (ETH #2), LiteCoin (LTC #9), Monero (XMR ), ZCash (ZEC), DigiByte (DGB), Argentum (ARG), among others.
![image alt <](/Images/class_0.PNG)<br />
- **Class 1**
![image alt <](/Images/class_1.PNG)<br />
- **Class 2** there is only one currency: BitTorrent (BTT).  BitTorrent is an important component on Cryptocurrencies.  However, it stands alone and it has a very large z-score of 21.59 (please look at the code for the z-score).
- **Class 3:** there are only four cryptocurrencies: POA(# 666), AAC (#1230), BBP (# 1589) and  WAVES (# 80)
![image alt <](/Images/class_3.PNG)<br />

## 2D-Scatter plot with TotalCoinMined vs TotalCoinSupply
![image alt <](/Images/box_plot.PNG)<br />

Plotting the scatter plot from two cryptocurrency features directly does not efficiently segregate the different classes. Then using the PCA algorithm is the right method for better visualizations.


# Summary
We have identified the classification of 532 cryptocurrencies based on similarities of their features.

Particularities of each group need to be analyzed to determine their performance and potential interest for the investment bank's clients. 
I would strongly suggest that we further investigate the CoinShares MarketCap to further identify which cryptocurrencies have liquidity and are relevant to investors.  Based on our analysis, Class “0” has the well-known crypto currencies like BTC (BitCoin), Ethereum (ETH), LiteCoin (LCC).  

Further data is deemed necessary to determine if it is suitable to investment based on:
- Market Cap
- Trading Volume
- Circulating Supply
- Volatility
- Research coverage

