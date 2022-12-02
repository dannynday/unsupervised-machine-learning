# Module 10 Challenge: Crypto Clustering

![Decorative image.](Images/10-5-challenge-image.png)

## Background

In this Challenge, I will assemble investment portfolios that are based on cryptocurrencies. Instead of basing my proposal on only returns and volatility, I want to include other factors that might impact the crypto market&mdash;leading to better performance for a portfolio.


## What am I Creating

In this Challenge, I will combine my financial Python programming skills with the new unsupervised learning skills.

I will create a Jupyter notebook that clusters cryptocurrencies by their performance in different time periods. I will then plot the results.

The provided CSV file contains the price change data of cryptocurrencies in different periods.

### Find the Best Value for k Using the Original Data

In this section, I will use the elbow method to find the best value for k.

1. Code the elbow method algorithm to find the best value for k. Use a range from 1 to 11.

2. Plot a line chart with all the inertia values computed with the different values of k to visually identify the optimal value for k.

3. Answer the following question: What is the best value for k?

### Cluster Cryptocurrencies with K-means Using the Original Data

In this section, I will use the K-means algorithm with the best value for k (found in the previous section) in order to cluster the cryptocurrencies according to the price changes of cryptocurrencies provided.

1. Initialize the K-means model with four clusters by using the best value for k.

2. Fit the K-means model using the original data.

3. Predict the clusters to group the cryptocurrencies using the original data. View the resulting array of cluster values.

4. Create a copy of the original data and add a new column with the predicted clusters.

5. Using hvPlot, create a scatter plot by setting `x="price_change_percentage_24h"` and `y="price_change_percentage_7d"`. Color the graph points with the labels found using K-means. Then, add the crypto name in the `hover_cols` parameter to identify the cryptocurrency represented by each data point.

### Optimize Clusters with Principal Component Analysis

In this section, I will perform a principal component analysis (PCA) and reduce the features to three principal components.

1. Create a PCA model instance and set `n_components=3`.

2. Use the PCA model to reduce to three principal components. View the first rows of the DataFrame.

3. Retrieve the explained variance to determine how much information can be attributed to each principal component.

4. Answer the following question: What is the total explained variance of the three principal components?

5. Create a new DataFrame with the PCA data. Set the `coin_id` index from the original DataFrame as the index for the new DataFrame. Review the resulting DataFrame.

### Find the Best Value for k Using the PCA Data

In this section, I will use the elbow method to find the best value for k by using the PCA data.

1. Code the elbow method algorithm and use the PCA data to find the best value for k. Use a range from 1 to 11.

2. Plot a line chart with all the inertia values computed with the different values of k to visually identify the optimal value for k.

3. Answer the following questions: What is the best value for k when using the PCA data? Does it differ from the best k value found using the original data?

### Cluster Cryptocurrencies with K-means Using the PCA Data

In this section, I will use the PCA data and the K-means algorithm with the best value for k (found in the previous section) in order to cluster the cryptocurrencies according to the principal components.

1. Initialize the K-means model with four clusters by using the best value for k.

2. Fit the K-means model by using the PCA data.

3. Predict the clusters to group the cryptocurrencies by using the PCA data. View the resulting array of cluster values.

4. Create a copy of the DataFrame with the PCA data and add a new column to store the predicted clusters.

5. Using hvPlot, I will create a scatter plot by setting `x="price_change_percentage_24h"` and `y="price_change_percentage_7d"`. Color the graph points with the labels found using K-means. Then, add the crypto name in the `hover_cols` parameter to identify the cryptocurrency represented by each data point.

### Visualize and Compare the Results

In this section, I will visually analyze the cluster analysis results by observing the outcome with and without using the optimization techniques.

1. Create a composite plot using hvPlot and the plus (`+`) operator to compare the elbow curve that I created to find the best value for k with the original data and the PCA data.

2. Create a composite plot using hvPlot and the plus (`+`) operator to compare the cryptocurrencies clusters using the original data and the PCA data.

3. Answer the following question: After visually analyzing the cluster analysis results, what is the impact of using fewer features to cluster the data by using K-means?

 create composite plots. here is [the hvPlot documentation](https://holoviz.org/tutorial/Composing_Plots.html).
