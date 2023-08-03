# CryptoClustering
UNC_data_bootcamp_module_19

## Challenge Description
### Background
For this challenge, we need to use our knowledge of Python via a Jupyter Notebook and Unsupervised Learning to predict if cryptocurrencies are affected by 24-hour or 7-day price changes.



## Deliverables
Our goal for this challenge is multi-part. We will need to find the best k value using a Scaled DataFrame created from the source CSV file. (Add rest later)


### Section-1: Prepare the Data
To start off I needed to rename the __Crypto_Clustering_starter_code.ipynb__ file as __Crypto_Clustering_SDT.ipynb__. I viewed the file _crypto_market_data.csv_ separately first to understand the data scource better, then I loaded the _crypto_market_data.csv_ into a DataFrame. From here I am able to acquire the metrics and plot the data needed complete the challenge per the instructions:
* Use the _StandardScaler()_ module from _scikit-learn_ to normalize the data from the CSV file.
* Create a DataFrame with the scaled data and set the __"coin_id"__ index from the original DataFrame as the index for the new DataFrame.

![First DataFrame] placeholder???


### Section-2: Find the Best Value for k Using the Original Scaled DataFrame
In this section I will use the elbow method to find the best value for _k_ per the instructions from the challenge:
* Create a list with the number of k values from 1 to 11.
* Create an empty list to store the inertia values.
* Create a _for_ loop to compute the inertia with each possible value of _k_.
* Create a dictionary with the data to plot the elbow curve.
* Plot a line chart with all the inertia values computed with the different values of _k_ to visually identify the optimal value for _k_.
* Answer the following question in your notebook: What is the best value for _k_?


### Section-3: Cluster Cryptocurrencies with K-means Using the Original Scaled Data
For this section I will use the following steps per the challenge instructions to cluster the cryptocurrencies for the best value for _k_ of the original scaled data:
* Initialize the K-means model with the best value for _k_.
* Fit the K-means model using the original scaled DataFrame.
* Predict the clusters to group the cryptocurrencies using the original scaled DataFrame.
* Create a copy of the original data and add a new column with the predicted clusters.
* Create a scatter plot using hvPlot as follows:
  * Set the x-axis as __"PC1"__ and the y-axis as __"PC2"__.
  * Color the graph points with the labels found using K-means.
  * Add the __"coin_id"__ column in the _hover_cols_ parameter to identify the cryptocurrency represented by each data point.




### Section-4: Optimize Clusters with Principal Component Analysis
In this section I will further refine the clusters using Principal Component Analysis (__PCA__) per the challenge instructions:
* Using the original scaled DataFrame, perform a PCA and reduce the features to three principal components.
* Retrieve the explained variance to determine how much information can be attributed to each principal component and then answer the following question in your notebook:
  * _What is the total explained variance of the three principal components_?
* Create a new DataFrame with the PCA data and set the __"coin_id"__ index from the original DataFrame as the index for the new DataFrame.

![PCA DataFrame] placeholder




### Section-5: Find the Best Value for k Using the PCA Data
Following challenge instructions I will again use the elbow method on the PCA data to find the best value for _k_ by:
* Create a list with the number of k-values from 1 to 11.
* Create an empty list to store the inertia values.
* Create a _for_ loop to compute the inertia with each possible value of _k_.
* Create a dictionary with the data to plot the Elbow curve.
* Plot a line chart with all the inertia values computed with the different values of _k_ to visually identify the optimal value for _k_.
* Answer the following question in your notebook:
  * What is the best value for _k_ when using the PCA data?
  * Does it differ from the best k value found using the original data?



### Section-6: Cluster Cryptocurrencies with K-means Using the PCA Data
Finally, I will complete the following steps per the challenge instructions to cluster the cryptocurrencies for the best value for _k_ on the PCA data:
* Initialize the K-means model with the best value for _k_.
* Fit the K-means model using the PCA data.
* Predict the clusters to group the cryptocurrencies using the PCA data.
* Create a copy of the DataFrame with the PCA data and add a new column to store the predicted clusters.
* Create a scatter plot using hvPlot as follows:
  * Set the x-axis as __"price_change_percentage_24h"__ and the y-axis as __"price_change_percentage_7d"__.
  * Color the graph points with the labels found using K-means.
  * Add the __"coin_id"__ column in the _hover_cols_ parameter to identify the cryptocurrency represented by each data point.
* Answer the following question:
  * What is the impact of using fewer features to cluster the data using K-Means?




## Resources
### Bootcamp References --- Update for this Challenge!!
Module 19 Instructions
 
starter_code
* Crypto_Clustering_starter_code.ipynb

Resources
* crypto_market_data.csv


 
***Special Thanks:***
* Jamie Miller
* Mounika Mamindla
* Lisa Shemanciik
 
### External References
_(where possible will provide link to website)_
* [pandas documentation](https://pandas.pydata.org/docs/reference/general_functions.html)
* [matplotlib documentation](https://matplotlib.org/stable/index.html)
* [hvplot documentation](https://hvplot.holoviz.org/reference/geopandas/points.html)
* [scipy.stats documentation](https://docs.scipy.org/doc/scipy/reference/stats.html)



