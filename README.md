# vertexUserClassification
Applying Cluster Analysis to Classify Users of a DeFi Protocol

This project applies K-means clustering to identify distinct groups of traders based on their transactional behavior. The analysis utilizes Flipside Crypto's API to retrieve trader data and leverages the "elbow method" to determine the optimal number of clusters.

Project components:
 - README.md: This file, providing project documentation and instructions.
 - vertexUserClassification.ipynb: Python script containing data analysis, clustering, PCA, and visualization.
 - clustered_trader_data.csv: Output file containing the original trader data with assigned cluster labels.
    
Requirements:
 - Flipside account (API)
 - python, pip, jupyter notebook (any other working environment)

Instruction:
 - create an SQL query to collect data of protocol activities on Flipside
 - create and activate a virtualenv

Working notebook
Data Source: 
This analysis uses data from the Flipside Crypto API, fetched from:
    
    https://flipsidecrypto.xyz/api/v1/queries/689c3560-0152-488d-851f-eff12dcc8a58/data/latest

Step-by-Step Analysis:
 - import Libraries & Load Data: 
 - import necessary libraries, fetch trader data from the API, and create a pandas DataFrame.

Data Preprocessing: 
exclude the TRADER column and standardize numerical features for fair comparison during clustering.

Elbow Method for Optimal Clusters:
determine the optimal number of clusters using the elbow method (visualize WCSS vs. the number of clusters.

K-means Clustering: 
apply K-means clustering with the chosen number of clusters (4 in this example) and assign cluster labels to each trader.

Cluster Analysis:
 - Calculate and print the mean values for each feature within each cluster.
 - Show the size of each cluster.

PCA Analysis:
 - initialize PCA with a desired explained variance ratio of 95%.
 - transform the scaled data into principal components.
 - print explained variance ratios and plot the cumulative explained variance.
 - create a DataFrame with principal components and cluster labels for plotting.
 - generate scatter plots to visualize clusters in the PCA space.
      
Save Results: 
Save the DataFrame with cluster labels to a CSV file (clustered_trader_data.csv).

Running the Analysis:
 - clone Repository: Clone this repository.
 - execute Script: Run the script.

Interpreting Results:
Elbow Plot: 
use it to determine the "optimal" number of clusters, balancing model complexity and information capture.

Cluster Analysis Table: 
examine the mean feature values in each cluster to understand their distinct characteristics.

PCA Plots: 
visualize how traders are grouped in the principal component space. Each principal component represents a combination of original features, and clusters indicate distinct trader behaviors.

Important Note: 
The PCA analysis might require additional fine-tuning of the desired_variance_ratio depending on the data's dimensionality and your analysis goals.
