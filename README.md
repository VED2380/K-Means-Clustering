# K-Means Clustering on Mall Customers

## Overview

This project applies the **K-Means clustering** algorithm on customer data from a shopping mall to identify distinct customer segments based on their **Annual Income** and **Spending Score**. The analysis helps visualize how customers group naturally, aiding in targeted marketing.

## Files

- `Mall_Customers.csv` — Dataset containing customer demographics and behavior.
- `k_means_clustering.ipynb` — Jupyter notebook implementing the clustering analysis.
- `Mall_Customers_with_Clusters.csv` (optional) — Final dataset with cluster labels (if saved).

## Steps in the Notebook

1. **Data Loading and Preparation**  
   - Imports the dataset using `pandas`
   - Selects `Annual Income (k$)` and `Spending Score (1-100)` as clustering features
   - Scales the features using `StandardScaler`

2. **Finding Optimal K (Elbow Method)**  
   - Iteratively fits K-Means for `K = 1 to 10`
   - Plots inertia to identify the "elbow point" (typically at K=5)

3. **Model Fitting with K=5**  
   - Clusters customers using `KMeans(n_clusters=5)`
   - Predicts and assigns cluster labels

4. **Visualization**  
   - Plots a scatterplot of `Annual Income` vs. `Spending Score` with color-coded clusters
   - Shows cluster centroids in red

5. **Evaluation**  
   - Calculates **Silhouette Score** to assess clustering quality  
     _Result: `Silhouette Score for K=5: ~0.555`_

## Libraries Used

- `pandas`
- `matplotlib`
- `scikit-learn`
- `numpy`

## How to Run

1. Clone this repository
2. Launch Jupyter Notebook or JupyterLab
3. Open `k_means_clustering.ipynb` and run all cells
