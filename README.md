# Unsupervised Machine Learning - Cryptocurrency Clusters

### Background
Unsupervised Learning is a machine learning technique in which the users do not need to supervise the model. Instead, it allows the model to work on its own to discover patterns and information that was previously undetected. It mainly deals with the unlabelled data.

Here, are prime reasons for using Unsupervised Learning in Machine Learning:
* Unsupervised machine learning finds all kind of unknown patterns in data.
* Unsupervised methods help you to find features which can be useful for categorization.
* It is taken place in real time, so all the input data to be analyzed and labeled in the presence of learners.
* It is easier to get unlabeled data from a computer than labeled data, which needs manual intervention.

### Applications of Unsupervised Machine Learning
Some application of Unsupervised Learning Techniques are:
* Clustering automatically split the dataset into groups base on their similarities.
* Anomaly detection can discover unusual data points in your dataset. It is useful for finding fraudulent transactions.
* Association mining identifies sets of items which often occur together in your dataset.
* Latent variable models are widely used for data preprocessing. Like reducing the number of features in a dataset or decomposing the dataset into multiple components.

### Instructions - Data Preparation
1. We are given raw data, so first we need to process it to fit the machine learning models. Since there is no known classification system, we need to use unsupervised learning. we will use several clustering algorithms to explore whether the cryptocurrencies can be grouped together with other similar cryptocurrencies. We use data visualization to share our findings with the investment bank.
2. Read crypto_data.csv into Pandas.
3. Discard all cryptocurrencies that are not being traded. Then drop the IsTrading column from the dataframe.
4. Remove all rows that have at least one null value.
5. Filter for cryptocurrencies that have been mined. That is, the total coins mined should be greater than zero.
6. Since the coin names do not contribute to the analysis of the data, delete the CoinName from the original dataframe.
7. Convert the remaining features with text values, Algorithm and ProofType, into numerical data.
8. Standardize your dataset so that columns that contain larger values do not unduly influence the outcome.

### Dimensionality Reduction
* Creating dummy variables above dramatically increased the number of features in the dataset. Perform dimensionality reduction with PCA.  It is possible to state the desired explained variance. For example, say that a dataset has 100 features. Using PCA(n_components=0.99) creates a model that will preserve approximately 99% of the explained variance, whether that means reducing the dataset to 80 principal components or 3. 
* Next, further reduce the dataset dimensions with t-SNE and visually inspect the results.

### Cluster Analysis with k-Means
Create an elbow plot to identify the best number of clusters

![ElbowCuve_KMeans](https://user-images.githubusercontent.com/85952426/170316440-b7f84c0d-bbe8-4cef-a6e3-4dac1cba8006.png)

The best k value is 4 so we will get an output of 4 clusters to categorize the crytocurrencies.


### Visualizations
1. 2D-Scatter plot with clusters: Two Components

![hvplot scatter(2)](https://user-images.githubusercontent.com/85952426/170317710-0c875fc1-fea1-4411-9e1b-b960b1ab4d25.png)

2. 3D-Scatter plot with clusters: Three Components

![3D_PCA_Clusters](https://user-images.githubusercontent.com/85952426/170318330-10ea9e3d-e6b9-42a4-af04-c4a09792f948.png)

3. 2D-Scatter plot using x="TotalCoinsMined" and y="TotalCoinSupply"

![hvplot scatter](https://user-images.githubusercontent.com/85952426/170320962-ea275bca-e713-4f72-abda-95fc9bba19c2.png)










