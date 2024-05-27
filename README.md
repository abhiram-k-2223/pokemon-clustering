# Pokemon Clustering

## Overview

This project performs clustering analysis on a Pokémon dataset using K-Means clustering. The dataset is preprocessed, and various analyses are conducted to determine the optimal number of clusters. The clustering results are visualized, and cluster centroids are extracted for interpretation.

## Dataset

The dataset used in this project is a CSV file named `pokemon.csv`. It contains information about various Pokémon, including their types, stats, and other attributes.

## Steps

### 1. Importing Libraries
- Essential libraries such as `pandas`, `matplotlib`, `seaborn`, and `sklearn` are imported.

### 2. Loading the Dataset
- The dataset is loaded into a DataFrame using `pandas`.

### 3. Data Inspection and Cleaning
- The first few rows of the dataset are displayed to understand its structure.
- Missing values in the dataset are identified and visualized using a bar plot.
- All missing values are filled with zeros for simplicity.

### 4. Data Preprocessing
- The categorical columns 'Type 1' and 'Type 2' are converted to categorical data types.
- Label encoding is applied to transform categorical data into numerical values for clustering.

### 5. Feature Selection
- Columns that are not required for clustering ('Name' and 'Legendary') are dropped.

### 6. K-Means Clustering
- The optimal number of clusters is determined using the Elbow Method.
  - K-Means clustering is applied for cluster numbers ranging from 1 to 10.
  - The within-cluster sum of squares (WCSS) for each number of clusters is calculated and plotted.
- Based on the Elbow Method plot, 6 clusters are chosen for the final model.
- K-Means clustering is performed with 6 clusters, and the resulting cluster labels are added to the DataFrame.

### 7. Cluster Visualization
- A pair plot is generated using `seaborn` to visualize the clusters with respect to various features.
- The centroids of the clusters are extracted and displayed.

### 8. Evaluation
- The silhouette score, which measures how similar an object is to its own cluster compared to other clusters, is calculated for cluster numbers ranging from 2 to 10.
- The silhouette scores for each number of clusters are displayed to evaluate clustering performance.

## Results
- The dataset is successfully clustered into 6 groups.
- Cluster centroids are extracted for further analysis.
- The silhouette scores help in evaluating the quality of clustering.

## Visualization
- The Elbow Method plot shows the WCSS for different numbers of clusters, helping to determine the optimal cluster count.
- The pair plot visualizes the distribution of data points across the clusters.
- Silhouette scores for different cluster numbers provide insight into clustering quality.

## Conclusion
The K-Means clustering analysis effectively groups the Pokémon dataset into meaningful clusters, providing insights into the underlying patterns and relationships within the data. The visualizations and cluster centroids further enhance the understanding of these groups.

## Dependencies
- pandas
- matplotlib
- seaborn
- sklearn

To run the analysis, ensure all dependencies are installed and the dataset `pokemon.csv` is available in the working directory. The code can be executed in a Python environment or Jupyter Notebook.
