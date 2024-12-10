Clustering is an unsupervised learning technique used in machine learning to group data points into clusters based on their similarities. Unlike supervised learning, 
clustering does not require labeled data; instead, it identifies patterns or structures within the dataset.<br><br>

<h3><b>Key Concepts in Clustering</b></h3>
<ul>
<li>Clusters: Groups of data points that are more similar to each other than to points in other groups. Similarity is typically measured using a distance metric like 
  Euclidean distance.</li>
  
<li>Centroid: The center of a cluster. In algorithms like K-Means, centroids are calculated iteratively to minimize the distance of points within the cluster.</li>

<li>Inertia: A measure of how well data points are clustered. Lower inertia indicates better-defined clusters. It represents the sum of squared distances between 
  points and their centroids.</li>

<li>Inter-cluster Distance: The distance between the centroids of different clusters. Higher inter-cluster distance indicates well-separated clusters.</li>
</ul>

<h3><b>Common Clustering Algorithms</b></h3>
<ol type='1'>
<li><b>KMeans Clustering:</b> KMeans is a popular unsupervised learning algorithm used for clustering, where the goal is to group data into distinct clusters
  based on their similarity. It minimizes the variance within each cluster and maximizes the variance between clusters.<br>

  Working:<br>
  <ul>
<li>Choose the number of clusters k and randomly initialize k cluster centroids (mean points).</li>
<li>Assign each data point to the cluster with the nearest centroid. The distance is typically measured using Euclidean distance.</li>
<li>Recalculate the centroids of the clusters based on the current assignments. The new centroid is the mean of all points in the cluster.</li>
<li>Alternate between the assignment and update steps until the centroids stabilize or maximum iterations are reached.</li>
<li>Final cluster assignments and centroids are the output.</li>
</ul></li><br>

<li><b>Hierarchical Clustering:</b> Hierarchical Clustering is a method of grouping data points into clusters based on their similarity. It builds a hierarchy 
  (tree-like structure) of clusters, which is visualized using a dendrogram. A dendrogram is a tree-like diagram that shows the sequence of merges and the 
  distances at which clusters are merged.<br>

  There are two main approaches:<br>
  <ul>

<li><b>Agglomerative (Bottom-Up):</b> Starts with each data point as its own cluster. Gradually merges the closest clusters until all points are in a single 
  cluster.</li>
  
<li><b>Divisive (Top-Down):</b> Starts with all points in one large cluster. Recursively splits clusters into smaller ones.></li>
</ul>

Agglomerative Clustering is more common, Steps:
<ul>
<li>Calculate Pairwise Distances: Compute the distance between every pair of data points using a metric like Euclidean distance.</li>
<li>Create Clusters: Start with each data point as its own cluster.</li>
<li>Merge Clusters: Iteratively merge the two closest clusters based on their distance until all points belong to one single cluster.</li>
<li>Define Linkage: Choose a linkage criterion to determine the distance between clusters:
  <ul>
<li>Single Linkage: Distance between the nearest points in two clusters. (Mostly used)</li>
<li>Complete Linkage: Distance between the farthest points in two clusters.</li>
<li>Average Linkage: Average distance between all points in two clusters.</li></li>
  </ul>
<li><b>Instead of considering all points as a single cluster, we cut the dendrogram at an appropriate level to decide the number of clusters based on the distances 
  where merges occur.</b></li>
</ul>
</li><br>

<li><b>DBSCAN Clustering (Density-Based Spatial Clustering of Applications with Noise):</b> It is a powerful clustering algorithm used to identify clusters of 
  varying shapes and densities in a dataset. Unlike KMeans or hierarchical clustering, DBSCAN does not require you to specify the number of clusters in advance. 
  Instead, it groups points that are close to each other based on a density criterion and can also identify noise (outliers). Can identify clusters of arbitrary 
  shapes, unlike KMeans, which assumes spherical clusters.<br>

  Key Concepts in DBSCAN:<br>
  <ul>
<li>Epsilon (ε): The radius around a data point to search for neighboring points. Determines how close points should be to be considered part of the same cluster.</li>
<li>MinPts (Minimum Points): The minimum number of points required to form a dense region (i.e., a cluster). Includes the point itself.</li>
<li>Core Point: A point with at least MinPts neighbors within ε.</li>
<li>Border Point: A point that is not a core point but falls within the ε-radius of a core point.</li>
<li>Noise: Points that are neither core nor border points.</li>
</ul>

Steps in DBSCAN:<br>
<ul>
<li>Identify Core Points: For each point, check if it has at least MinPts neighbors within the distance ε.</li>
<li>Expand Clusters: Start from an unvisited core point and recursively include all its density-reachable neighbors.</li>
<li>Mark Outliers: Points that cannot be reached from any core point are labeled as outliers (noise).</li>
</ul>
</li>
</ol>

<h3><b>When to Use Clustering</b></h3>
<ul>
<li>When you have unlabeled data.</li>
<li>To identify groups or patterns within data (e.g., customer segmentation, anomaly detection, image compression).</li>
</ul>

<h3><b>Applications</b></h3>
<ul>
<li>Marketing: Segment customers based on purchasing behavior.</li>
<li>Biology: Group genes with similar functions.</li>
<li>Image Processing: Compress images by reducing colors.</li>
<li>Anomaly Detection: Identify unusual patterns in data.</li>
</ul>


