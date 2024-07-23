# CryptoClustering
Overview
This project classifies cryptocurrencies based on their price fluctuations across various timeframes using K-means clustering and Principal Component Analysis (PCA). The analysis examines price changes over intervals of 24 hours, 7 days, 30 days, 60 days, 200 days, and 1 year to identify patterns and group similar cryptocurrencies.

Repository Setup
A new repository named CryptoClustering was created on GitHub.
The repository was cloned to the local machine.
All changes were regularly pushed to GitHub.
Files and Initial Setup
The provided starter files were downloaded and placed in the project directory.
The Crypto_Clustering_starter_code.ipynb file was renamed to Crypto_Clustering.ipynb.
The crypto_market_data.csv file was loaded into a Pandas DataFrame with coin_id set as the index.
Summary statistics of the data were reviewed to understand its structure.

Data Preparation
The data was normalized using the StandardScaler module from scikit-learn.
A new DataFrame was created to store the scaled data, with coin_id as the index.
Finding the Best Value for k

Elbow Method:
A list of k values ranging from 1 to 11 was created.
Inertia for each k value was computed and stored.
Inertia values were plotted to identify the optimal k.
The optimal value for k was determined by visually inspecting the elbow curve.
Clustering with K-Means

Original Scaled Data:
The K-means model was initialized with the optimal k value.
The model was fitted to the scaled data.
Clusters for the cryptocurrencies were predicted.
The predicted cluster labels were added to the original DataFrame.
A scatter plot of the clusters was created using price_change_percentage_24h and price_change_percentage_7d.
Principal Component Analysis (PCA)

Performing PCA:
Features were reduced to three principal components.
The explained variance was calculated to determine the information retained by each component.
A new DataFrame was created with the PCA-transformed data, retaining coin_id as the index.
Finding the Best Value for k with PCA Data

Elbow Method with PCA Data:
The elbow method steps were repeated using the PCA-transformed data to find the optimal k.
The best k value from the PCA data was compared with the original data.
Clustering with K-Means on PCA Data

PCA Data:
The K-means model was initialized and fitted with the optimal k value using the PCA data.
Clusters were predicted and added to the PCA DataFrame.
A scatter plot of the clusters was created using PC1 and PC2.
Feature Weights and Influence

Determining Feature Weights:
A DataFrame was created showing the weights of each feature for each principal component.
Features with the strongest positive or negative influence on each component were identified.

Key Findings and Visualizations
Finding the Best Value for k Using the Original Scaled DataFrame
The elbow method was used to determine the optimal k value.
The best value for k was identified and documented.
Clustering Cryptocurrencies with K-Means Using the Original Scaled Data
The K-means model was fitted and clusters were predicted.
A scatter plot was created to visualize the clusters.
Optimizing Clusters with PCA
PCA reduced the features to three principal components.
The total explained variance of the three principal components was calculated.
A PCA DataFrame was created.
Finding the Best Value for k Using the PCA Data
The elbow method with PCA data was used to determine the best k value.
The best k value from PCA data was compared with the original data.
Clustering Cryptocurrencies with K-Means Using the PCA Data
The K-means model was fitted using PCA data and clusters were predicted.
A scatter plot was created to visualize the clusters.
Feature Weights and Influence
A DataFrame showing feature weights for each principal component was created.
Features with the strongest influence on each component were identified.

Conclusion
The CryptoClustering project successfully classified cryptocurrencies based on their price fluctuations using K-means clustering and PCA. The analysis provided insights into optimal clustering and the influence of various features on the classification process. The results and visualizations are documented and available in the GitHub repository.
