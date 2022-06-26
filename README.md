# Cryptocurrencies
Unsupervised Machine Learning for Cryptocurrency Project

# Overview

Utilizing unsupervised machine learning, our client, Martha, with Accountability Accounting, requests a report that shows which cryptocurrencies are trading and if they can be grouped into a classificiation system.  

# Results

The data was obtained from [CryptoCompare](https://min-api.cryptocompare.com/data/all/coinlist).  The first steps include reading the data into a pandas DataFrame and learning about the data.  This step is preprocessing the data so that it can be utilized in the machine learning algorithms. The following modificiations were performed on the dataset: 
1. Only kept those currencies that are being traded. 
2. Only kept those currencies with a working algorithm
3. Removed rows that had at least one null value. 
4. Kept the rows where coins are mined. 
5. Using pandas.get_dummies, the categorical data in Algorithm and ProofType were converted to indicator variables. 
6. 
