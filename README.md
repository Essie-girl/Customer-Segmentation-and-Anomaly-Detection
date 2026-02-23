# Customer Segmentation and Anomaly Detection

## Project Overview
This project focuses on analyzing customer data from a mall to perform customer segmentation and identify potential anomalies. By segmenting customers, businesses can tailor marketing strategies, improve customer experience, and optimize resource allocation. Anomaly detection helps in identifying unusual customer behaviors, which could indicate fraudulent activities or unique customer needs.

## Dataset
The dataset used is `Mall_Customers.csv`, containing information about mall customers, including `CustomerID`, `Genre`, `Age`, `Annual Income (k$)`, and `Spending Score (1-100)`.

## Features
- **Data Loading and Inspection**: Loading the dataset and performing initial checks on its structure, types, and missing values.
- **Exploratory Data Analysis (EDA)**: Visualizing the distribution of key features like Annual Income and Spending Score to understand their characteristics.
- **Feature Engineering**: Selecting relevant features and applying Standard Scaling to normalize the data for clustering.
- **Optimal Cluster Determination**: Using the Elbow Method to find the optimal number of clusters for K-Means.
- **K-Means Clustering**: Applying the K-Means algorithm to segment customers based on their Annual Income and Spending Score.
- **Cluster Visualization**: Visualizing the identified customer segments.
- **Cluster Profiling**: Analyzing the characteristics (mean Annual Income, Spending Score, and size) of each cluster.
- **Model Evaluation**: Assessing the quality of the clustering using the Silhouette Score.
- **Anomaly Detection**: Employing Isolation Forest to detect anomalous customer data points.
- **Anomaly Visualization**: Visualizing the detected anomalies within the customer distribution.

##  Results

**Customer Segmentation**
The K-Means algorithm identified 5 distinct customer segments:

Cluster 0 (Mid-Range): Average income and spending.

Cluster 1 (High Spenders, High Income): Affluent customers with high spending habits.

Cluster 2 (High Spenders, Low Income): Customers with lower income but high spending scores, potentially indicating impulse buyers or those spending beyond their means.

Cluster 3 (Low Spenders, High Income): High-income customers with low spending scores, possibly careful shoppers or those who spend more elsewhere.

Cluster 4 (Low Spenders, Low Income): Lower income customers with low spending scores, likely budget-conscious shoppers.

**Silhouette Score**

The Silhouette Score for the clustering was 0.55, indicating a reasonably good separation between the clusters.

**Anomaly Detection**

Isolation Forest identified 10 anomalies (5% of the dataset as specified by contamination=0.05). These anomalies often represent customers with extremely high or low income/spending scores, deviating significantly from the main customer groups. For example, some anomalies include customers with very high income but low spending, or vice-versa.

**Future Work**

-Explore other clustering algorithms (e.g., DBSCAN, Hierarchical Clustering) and compare their performance.

-Develop strategies for how to specifically target each identified customer segment and how to handle anomalous customers.

-Build a recommendation system based on customer segments.
