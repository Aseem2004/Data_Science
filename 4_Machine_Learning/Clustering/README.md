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

Comparions between various Clustering Algorithms:<br>

  <table>
        <thead>
            <tr>
                <th>Aspect</th>
                <th>KMeans</th>
                <th>Hierarchical</th>
                <th>DBSCAN</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>Definition</td>
                <td>Partitional clustering algorithm that minimizes the distance of points to their cluster centroids.</td>
                <td>Clustering algorithm that creates a hierarchy of clusters using distance measures.</td>
                <td>Density-based clustering that identifies core, border, and noise points.</td>
            </tr>
            <tr>
                <td>Type</td>
                <td>Partitional</td>
                <td>Hierarchical (Agglomerative or Divisive)</td>
                <td>Density-Based</td>
            </tr>
            <tr>
                <td>Data Assumptions</td>
                <td>Assumes spherical clusters and equal variances.</td>
                <td>Can handle clusters of various shapes (depending on the linkage method).</td>
                <td>Handles arbitrary-shaped clusters.</td>
            </tr>
            <tr>
                <td>Parameters</td>
                <td>Number of clusters (k).</td>
                <td>Linkage method (single, complete, ward).</td>
                <td>Minimum samples (min_samples), distance threshold (eps).</td>
            </tr>
            <tr>
                <td>Scalability</td>
                <td>Highly scalable for large datasets.</td>
                <td>Less scalable, computationally intensive for large datasets.</td>
                <td>Efficient for small to medium datasets.</td>
            </tr>
            <tr>
                <td>Handling Outliers</td>
                <td>Sensitive to outliers, as centroids can be pulled by them.</td>
                <td>May group outliers into clusters depending on distance linkage.</td>
                <td>Effectively identifies outliers as noise.</td>
            </tr>
            <tr>
                <td>Cluster Shape</td>
                <td>Works best for spherical clusters.</td>
                <td>Can adapt to cluster shape based on linkage.</td>
                <td>Handles arbitrary cluster shapes well.</td>
            </tr>
            <tr>
                <td>Initial Centroids</td>
                <td>Requires initial centroid selection, sensitive to initialization.</td>
                <td>No centroids involved.</td>
                <td>No centroids involved.</td>
            </tr>
        </tbody>
    </table>

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

<h2><b>Note</b></h2>
Comparison of features between make_moons, make_blobs and make_classification:<br><br>

  <table>
        <thead>
            <tr>
                <th>Feature</th>
                <th>make_moons</th>
                <th>make_blobs</th>
                <th>make_classification</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>Purpose</td>
                <td>Generate crescent-shaped, non-linear datasets</td>
                <td>Generate isotropic Gaussian blobs for clustering</td>
                <td>Generate synthetic datasets for classification problems</td>
            </tr>
            <tr>
                <td>Clusters/Classes</td>
                <td>Always produces two interleaving moon-shaped clusters</td>
                <td>Produces a specified number of Gaussian clusters</td>
                <td>Produces samples belonging to a specified number of classes</td>
            </tr>
            <tr>
                <td>Linear Separability</td>
                <td>Not linearly separable</td>
                <td>Often linearly separable, depending on parameters</td>
                <td>Can create linearly or non-linearly separable data</td>
            </tr>
            <tr>
                <td>Parameters</td>
                <td>n_samples, noise, random_state</td>
                <td>n_samples, centers, cluster_std, random_state</td>
                <td>n_samples, n_features, n_informative, n_classes, etc.</td>
            </tr>
            <tr>
                <td>Use Case</td>
                <td>Testing non-linear classification algorithms</td>
                <td>Benchmarking clustering algorithms</td>
                <td>Benchmarking classification algorithms</td>
            </tr>
          <tr>
            <td>x shape</td>
            <td>(n_samples,2)</td>
            <td>(n_samples, n_features)</td>
            <td>(n_samples, n_features)</td>
          </tr>
          <tr>
            <td>y shape</td>
            <td>(n_samples,)</td>
            <td>(n_samples,)</td>
            <td>(n_samples,)</td>
          </tr>
        </tbody>
  </table>
