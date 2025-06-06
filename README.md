# AIML_Internship_Task8
# Mall Customer Segmentation using K-Means Clustering

This task performs customer segmentation on the Mall Customers dataset using the **K-Means clustering algorithm**.

## Steps Performed

### 1. Load Dataset
- Loaded the dataset using `pandas`.
- Selected two features relevant for clustering: **Annual Income** and **Spending Score**.

### 2. Feature Standardization
- Standardized the features using `StandardScaler` from `scikit-learn`.
- Standardization is necessary because K-Means uses Euclidean distance, which is sensitive to the scale of features.
- This step transforms data to have zero mean and unit variance, ensuring fair distance measurement.

### 3. Find Optimal Number of Clusters (Elbow Method)
- Trained K-Means models for cluster counts ranging from 1 to 10.
- Calculated and plotted **inertia** (sum of squared distances of samples to their closest cluster center) for each value of k.
- The plot helps identify the “elbow point” where adding more clusters does not significantly reduce inertia, indicating the optimal number of clusters.

### 4. Fit K-Means with Chosen Number of Clusters
- Selected the optimal number of clusters (e.g., **k = 5** based on the elbow plot).
- Trained the K-Means model on the standardized data and assigned cluster labels to each customer.

### 5. Evaluate Clustering Quality (Silhouette Score)
- Calculated the **Silhouette Score**, which measures how similar an object is to its own cluster compared to other clusters.
- Score ranges from -1 to 1, where a higher score indicates better-defined clusters.

### 6. Visualize Clusters Using PCA
- Reduced the dimensionality of the standardized data to 2 principal components using **Principal Component Analysis (PCA)**.
- Plotted the clusters on a 2D scatter plot based on these components.
- This visualization helps to see how well the clusters are separated.
