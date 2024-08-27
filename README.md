## TODO
1. Each element should be split into separate parts inside the code, allowing it to run for different data.

### Data loader
1. The data loader is almost ready. Add some type of report after each data loading to save measurements and display them later.

### K-means clustering
1. Time consumption measuring. 
2. Save clustering data into a file. DONE saved into json type file for each clustering. 
3. Implement scores to measure if clustering was done correctly. To speed up this process, check if it is possible to use a subset of the map (e.g., 1/4 or 1/8) for clustering. 
4. Improve the plot to make elements clearer.

### Normalized cross-correlation on each cluster
1. Determine if this should be sourced from the kikuchipy library or implemented manually.
2. Consider writing the implementation by myself.

### Clustering performed on 1/4 of the map, with marked centroids.
    
![Clustering_results_with_centroids](/EBSD_analyze_app/final_pictures&data/centroids_map.png)
    
    
    
    Silhouette Score: 0.5917310508708085
    Calinski-Harabasz Score: 266.2677405472838
    Davies-Bouldin Score: 1.4054012791999773
    Inertia: 34624625535.088425




### Avreage picture inside one cluster 

# Clustering Evaluation Metrics

This document provides an overview of the clustering evaluation metrics used to assess the quality of clustering results. The metrics include the Elbow Method, Silhouette Score, Davies-Bouldin Index, and Calinski-Harabasz Index.

## Elbow Method

The Elbow Method is used to determine the optimal number of clusters by plotting the sum of squared distances (inertia) from each point to its assigned cluster center. The "elbow" point, where the rate of decrease sharply changes, indicates the optimal number of clusters.

![Elbow Method](EBSD_analyze_app/final_pictures&data/6bOEHyGv.jpg)

## Silhouette Score

The Silhouette Score measures how similar each point is to its own cluster compared to other clusters. The score ranges from -1 to 1, where a higher score indicates better-defined clusters.

![Silhouette Score](/EBSD_analyze_app/final_pictures&data/silhouette_score.svg)

## Davies-Bouldin Index

The Davies-Bouldin Index measures the average similarity ratio of each cluster with the cluster that is most similar to it. A lower Davies-Bouldin Index indicates better clustering.

![Davies-Bouldin Index](/EBSD_analyze_app/final_pictures&data/davies_bouldin_score.svg)

## Calinski-Harabasz Index

The Calinski-Harabasz Index measures the ratio of the sum of between-cluster dispersion and within-cluster dispersion. A higher Calinski-Harabasz Index indicates better-defined clusters.

![Calinski-Harabasz Index](/EBSD_analyze_app/final_pictures&data/calinski_harabasz_index.svg)

## Summary

- **Elbow Method**: Helps determine the optimal number of clusters.
- **Silhouette Score**: Measures the quality of clustering.
- **Davies-Bouldin Index**: Evaluates the average similarity ratio of clusters.
- **Calinski-Harabasz Index**: Assesses the ratio of between-cluster and within-cluster dispersion.
