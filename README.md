# CryptoClustering

This repository contains Python code for analyzing cryptocurrency market data using K-means clustering and principal component analysis (PCA). The analysis aims to identify patterns and clusters within the cryptocurrency market based on various features.

## Overview

The analysis involves the following steps:

1. **Data Loading and Exploration**: Initial loading of cryptocurrency market data from a CSV file and exploration of the dataset using summary statistics and visualization.

2. **Data Preprocessing**: Standardization of the data using the `StandardScaler` module from scikit-learn to prepare it for clustering.

3. **Determining the Best Value for k**: Utilizing the elbow method algorithm to find the optimal number of clusters (k) by evaluating the inertia values for different k values.

4. **Cluster Cryptocurrencies Using K-Means**: Implementing the K-means clustering algorithm to group cryptocurrencies into clusters based on their features. Visualizing the clusters using scatter plots.

5. **Optimizing Clusters with PCA**: Employing Principal Component Analysis (PCA) to reduce the dimensionality of the data and enhance clustering performance.

6. **Finding the Best Value for k Using PCA Data**: Similar to step 3, determining the optimal number of clusters using the PCA-transformed data.

7. **Cluster Cryptocurrencies Using PCA Data**: Performing K-means clustering on the PCA-transformed data and visualizing the clusters.

8. **Visualizing and Comparing Results**: Comparing the clustering results obtained from the original data and PCA-transformed data using composite plots.

## Analysis Summary

### Find the Best Value for k Using the Original Data

After conducting the K-means clustering analysis on the original data, the best value for `k` was determined to be 4.

### Optimize Clusters with Principal Component Analysis

Using Principal Component Analysis (PCA) to optimize the clusters, the total explained variance of the three principal components was found to be 0.8950316570309841.

### Find the Best Value for k Using the PCA Data

Upon applying PCA to the data, the best value for `k` was still determined to be 4, consistent with the analysis using the original data.

### Visualize and Compare the Results

When visually comparing the results, it was observed that the best value for `k` did not differ between the PCA-optimized clusters and the original data clusters.

## Resources

- **HoloViz Tutorial on Composing Plots**: The [HoloViz tutorial on composing plots](https://holoviz.org/tutorial/Composing_Plots.html) was referenced to learn how to create composite plots using hvPlot.

## Suppressing Warning Messages

To suppress FutureWarning and UserWarning messages, the following code is included in the script:

```python
import warnings
warnings.simplefilter(action='ignore', category=FutureWarning)
warnings.simplefilter(action='ignore', category=UserWarning)
