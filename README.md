# Cryptocurrencies
Unsupervised Machine Learning for Cryptocurrency Project

# Overview

Utilizing unsupervised machine learning, our client, Martha, with Accountability Accounting, requests a report that shows which cryptocurrencies are trading and if they can be grouped into a classificiation system.  

# Results

## Preprocess the Data

The data was obtained from [CryptoCompare](https://min-api.cryptocompare.com/data/all/coinlist).  The first steps include reading the data into a pandas DataFrame and learning about the data.  This step is preprocessing the data so that it can be utilized in the machine learning algorithms. The following modificiations were performed on the dataset: 
1. Only kept those currencies that are being traded. 
2. Only kept those currencies with a working algorithm
3. Removed rows that had at least one null value. 
4. Kept the rows where coins are mined. 
5. Using pandas.get_dummies, the categorical data in Algorithm and ProofType were converted to indicator variables. 
6. Scale the data using StandardScaler()

## Reduce the Data Dimensions using PCA

Once the data has been pre-processed, it needs to be evaluated to determine how many variables will be used to predict the model and how many classes or categories will be used to cluster the data. The instructions indicated that Principal Component Analysis PCA) should be used to reduce the components to 3 principal components. The  PCA algorithm is imported in the sklearn library. 

## Clustering Cryptocurrencies using K-Means

K-Means cluster method will cluster the unsupervised (or uncategorized) data into a user defined number of clusters.  One method to determine the appropriate number of clusters is to utilize the "Elbow Curve" where the scaled data from the PCA model are plotted and the inflection point is used to estimate the "correct" number of clusters. 

![ElbowCurve](https://user-images.githubusercontent.com/98054953/175830557-5b044c41-805a-45b4-8c64-ba911f028cfd.png)

As seen in the Elbow Curve, there is a change in the slope at K=4, so the analysis was run looking for 4 clusters. 

## Visualizing Cryptocurrencies Results

Once the K-Means analysis was run with 4 clusters, then the data can be plotted in a 3_D scatter plot. 

![3DScatter](https://user-images.githubusercontent.com/98054953/175830617-152429b4-8a87-49c2-9072-a2bc0211ddd4.png)

As requested by our client, a table was generated that has 532 tradable cryptocurrencies and is sortable by Coin Name, Algorithm, Proof Type, Total Coin Supply and Total Coins Mined. 

![TradableCurrencies](https://user-images.githubusercontent.com/98054953/175830668-d38fb801-5334-4cc6-8288-abdca75578f3.png)

Finally a graph was made of Total Coin Supply vs Total Coins Mined, with the ability to hover over the points and get the coin name and category. 

![CoinSupplyVsCoinsMined](https://user-images.githubusercontent.com/98054953/175830695-863efb24-09a9-41cd-8147-6db3fb412b90.png)

As the currency tables are updated, the analysis can continue to be refined and re-run to assist in the evaluation of the cryptocurrency market. 

