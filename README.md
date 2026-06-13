# MSCS_634_Lab3_Wine_Cluster_Evaluation

Lab 3: Clustering Analysis Using K-Means and K-Medoids Algorithms

Student Information

Name: Vamsi Matta
Course: Advanced Big Data and Data Mining (MSCS-634)
Assignment: Lab 3

⸻

Purpose of the Lab

The objective of this lab was to explore unsupervised machine learning techniques using clustering algorithms. The Wine dataset from the scikit-learn library was used to compare the performance of K-Means and K-Medoids clustering approaches. The analysis focused on cluster quality, visualization, and evaluation using Silhouette Score and Adjusted Rand Index (ARI).

⸻

Dataset Description

The Wine dataset contains chemical analysis measurements for wines belonging to three different categories. The dataset consists of 178 records and 13 numerical features.

The actual class labels were used only for evaluation purposes and were not included during clustering.

⸻

Methodology

1. Data Preparation

* Loaded the Wine dataset from scikit-learn.
* Examined dataset structure and feature statistics.
* Reviewed class distribution.
* Applied Z-score standardization using StandardScaler to normalize feature values.

2. Dimensionality Reduction

* Applied Principal Component Analysis (PCA) to reduce the dataset to two dimensions.
* PCA was used only for visualization and not for model training.

3. K-Means Clustering

* Implemented K-Means clustering with k = 3.
* Generated cluster assignments.
* Calculated:
    * Silhouette Score
    * Adjusted Rand Index (ARI)

4. K-Medoids Clustering

* Implemented a manual K-Medoids algorithm using pairwise distance calculations.
* Selected actual observations as medoids.
* Generated cluster assignments.
* Calculated:
    * Silhouette Score
    * Adjusted Rand Index (ARI)

5. Visualization

* Created PCA-based scatter plots for:
    * K-Means clusters
    * K-Medoids clusters
* Marked cluster centers for easier interpretation.

⸻

Key Results and Observations

* Standardization improved clustering consistency by placing all features on a common scale.
* PCA revealed visible grouping patterns among wine samples.
* K-Means created clusters using calculated centroids.
* K-Medoids created clusters using actual observations as representative medoids.
* Both algorithms successfully separated wine samples into three clusters.
* Silhouette Score was used to evaluate cluster separation and compactness.
* Adjusted Rand Index measured agreement between generated clusters and actual wine categories.

⸻

Challenges Encountered

The original plan was to use the KMedoids implementation from the scikit-learn-extra package. However, the package was not fully compatible with the local Python 3.14 environment and generated installation issues.

To satisfy the lab requirements while maintaining algorithm correctness, a manual K-Medoids implementation was developed using pairwise Euclidean distances. This approach follows the same core principles as the standard K-Medoids algorithm and produces valid clustering results.

⸻

Conclusion

This lab demonstrated how clustering algorithms can discover patterns in unlabeled data. Both K-Means and K-Medoids successfully grouped wine samples based on chemical characteristics.

K-Means provides efficient clustering through centroid optimization, while K-Medoids offers greater robustness by selecting actual observations as cluster representatives.

The combination of evaluation metrics and PCA visualizations provided a comprehensive comparison of clustering performance and helped identify the more effective model for the Wine dataset.

⸻

Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Scikit-learn
* Jupyter Notebook
* Visual Studio Code
* PCA
* K-Means Clustering
* Manual K-Medoids Clustering