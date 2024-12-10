Evaluation metrics are crucial to assess the performance of machine learning models. They differ based on the type of task: classification, regression, or other 
specialized problems like clustering.<br>

<h2><b>For Classification</b></h2>
<ul>
    <li><h3><b>Confusion Matrix</b></h3>
    Summarizes the classification results into:<br>
      <ul>
    <li>True Positives (TP): Correctly predicted positives.</li>
    <li>True Negatives (TN): Correctly predicted negatives.</li>
    <li>False Positives (FP): Incorrectly predicted as positive.</li>
    <li>False Negatives (FN): Incorrectly predicted as negative.</li></li>
    </ul>
  
  <li><h3><b>Accuracy</b></h3>
  The proportion of correctly predicted samples out of the total samples.<br>
  Accuracy = Total Predictions / Correct Predictions<br>
    Example: If a model predicts 95 out of 100 labels correctly, its accuracy is 95%.<br>
    
Interpretation: Higher accuracy indicates a better model, only if the dataset is balanced (classes are equally represented). For imbalanced datasets, high accuracy 
can be misleading (e.g., predicting the majority class always).</li>

<li><h3><b>Precision (Positive Predictive Value)</b></h3>
The ratio of true positive predictions to all positive predictions.<br>
Precision = TP / (TP + FP)<br>
  Example: If 100 instances are predicted positive and 80 are correct, precision = 80%.<br>
  
Interpretation: Higher precision means fewer false positives. Critical in scenarios like spam detection, where false positives (important emails marked as spam) are
costly. </li>

<li><h3><b>Recall (Sensitivity or True Positive Rate)</b></h3>
The ratio of true positive predictions to all actual positive cases.<br>
Recall = TP / (TP + FN)<br>
 Example: If 100 instances are positive and 90 are identified, recall = 90%.<br>

Interpretation: Higher recall means fewer false negatives. Important in scenarios like disease diagnosis, where missing positives (e.g., undiagnosed patients) is
critical.</li>

<li><h3><b>F1-Score</b></h3>
The harmonic mean of precision and recall.<br>
F1-Score = (2⋅Precision⋅Recall) / (Precision+Recall)<br>
Example: If precision = 80% and recall = 70%, F1-Score = 74.6%.<br>
  
Interpretation: Balances precision and recall, useful when both are equally important. A high F1-score indicates a model with a good balance of low false positives 
and false negatives.</li>
</ul>
<br>

<h2><b>For Regression</b></h2>
<ul>
    <li><h3><b>Mean Squared Error (MSE)</b></h3>
  Measures the average squared difference between predicted and actual values.<br>
    
  ![image](https://github.com/user-attachments/assets/026a367b-3c57-481d-93ab-189fe881a495)
    
  Interpretation: Smaller MSE indicates better predictions. Sensitive to outliers, as errors are squared. <b>Not directly interpretable in real world as errors are
  squared.</b></li>

<li><h3><b>Root Mean Squared Error (RMSE)</b></h3>
RMSE is the square root of the mean squared error (MSE). It measures the average magnitude of prediction errors, providing a metric in the same unit as the dependent
  variable<br>
  Example: Suppose a regression model predicts house prices. If the RMSE is 10,000 it means the model's average prediction error is about 10,000 units in the 
  currency of the house prices.<br>

  ![image](https://github.com/user-attachments/assets/7e5ebdb0-b4ad-43a1-884b-bc6a6aa0226d)

Interpretation: Lower RMSE indicates better fit and less deviation between predicted and actual values. It is sensitive to outliers because it squares the errors, 
magnifying larger errors. <b>RMSE is more interpretable in real-world contexts.</b>
 </li>

  <li><h3><b>Mean Absolute Error (MAE)</b></h3>
  Measures the average absolute difference between predicted and actual values.<br>
      
  ![image](https://github.com/user-attachments/assets/b27216d3-b276-4487-8759-33f9c5ac6e77)<br>
    
   Interpretation: Smaller MAE indicates better predictions. Less sensitive to outliers than MSE.</li>

<li><h3><b>R-squared (Coefficient of Determination)</b></h3>
Indicates the proportion of variance explained by the model. Range is 0 to 1.<br>
  
![image](https://github.com/user-attachments/assets/8712a659-8b60-4302-b634-845f5a408959)<br>

 Example: If y represents, say, the sales of a product, and the independent variables (predictors) are advertising spend and price, then:<br>
 R<sup>2</sup>=0.8 implies that 80% of the variation in sales is explained by advertising spend and price.<br>
20% of the variation in sales could be due to other factors like market trends, competition, or economic conditions not included in the model.<br>

Interpretation: R<sup>2</sup>=1: Perfect fit.<br>
R<sup>2</sup>=0: Model does not explain any variance.</li>
</ul>
<br>

<h2><b>For Clustering</b></h2>
<ul>
  <li><h3><b>Silhoutte Score</b></h3>
  Measures how similar an object is to its own cluster (cohesion) compared to other clusters (separation).<br>
  Silhoutte Score = (b-a) / max(a,b), where a: Average distance between a sample and all other points in its own cluster and b: Average distance between a sample
    and all points in the nearest cluster.<br>
Range: −1 to 1, where 1 indicates well-separated clusters and −1 suggests poor clustering.<br></li>

  <li><h3><b>Adjusted Rand Index (ARI)</b></h3>
  Measures the similarity between predicted clusters and true labels while correcting for chance.<br>
  Range: −1 (poor match) to 1 (perfect match).</li>

  <li><h3><b>Homogeneity, Completeness, V-Measure</b></h3>
      <ul>
  <li>Homogeneity (0-1): All points in a cluster belong to the same class. A Homogeneity score of 1 means that each cluster contains only members of a single class (perfectly homogeneous clustering). A Homogeneity score of 0 means that the clusters do not respect the true class labels at all (completely impure clusters).<br></li>
      
<li>Completeness(0-1): All points of a class are assigned to the same cluster. A Completeness score of 1 means that all data points of a true class are assigned to the same cluster. A Completeness score of 0 means that the true class is scattered across different clusters (complete disintegration).<br></li>

<li>V-Measure(0-1): Harmonic mean of homogeneity and completeness. A V-Measure score of 1 indicates perfect clustering (high Homogeneity and high Completeness).
A V-Measure score of 0 indicates poor clustering, where neither Homogeneity nor Completeness is satisfied.</li></li>
</ul>
  <li><h3><b>Inertia</b></h3>
It measures how tightly the points in a cluster are grouped around the center (centroid). Inertia is the sum of squared distances between each point and the centroid of the cluster to which it belongs. The lower the inertia, the better the clustering, because it indicates that points are closer to their respective centroids.<br>
  In ideal case, inertia = 0.</li>  
</ul>
