<h3><b>Support Vector Machine (SVM)</b></h3>

SVM is a supervised machine learning algorithm used for classification and regression tasks. It is particularly effective for high-dimensional datasets and 
scenarios where the number of dimensions exceeds the number of samples.<br>
The core idea of SVM is to find the optimal hyperplane that separates the data points of different classes with the maximum margin.

<h3><b>Key Concepts of SVM</b></h3>
<ul>
<li><b>Hyperplane:</b> A hyperplane is a decision boundary that separates data points belonging to different classes.<br>
In a 2D space, it's a line; in 3D, it's a plane; in higher dimensions, it's a generalization.<br>
The hyperplane equation is: f(x)=w⋅x+b where w is the weight vector, b is the bias, and x is the input.<br>
The hyperplane itself is the "decision function" where: w⋅x+b=0</li><br>

<li><b>Decision Boundaries:</b> The decision boundaries are defined by a margin around the hyperplane. In SVM, this margin ensures that the data points are 
  separated as widely as possible while maintaining correctness.<br>

The margin boundaries are:<br>

w⋅x+b=+1(Support vectors of Class 1) {w⋅x+b>+1: Class 1, for Binary Classification}<br>
w⋅x+b=−1(Support vectors of Class 2) {w⋅x+b<-1: Class 2, for Binary Classification}
</li>

![image](https://github.com/user-attachments/assets/b1facd8c-1a36-420f-84e9-ed0fcec4326b)<br>

<table border="1" style="border-collapse: collapse; width: 80%; text-align: left;">
  <caption><b>Differences Between Hyperplane and Decision Boundary</b></caption>
  <tr>
    <th>Aspect</th>
    <th>Hyperplane</th>
    <th>Decision Boundary</th>
  </tr>
  <tr>
    <td><b>Definition</b></td>
    <td>The central plane that separates the classes.</td>
    <td>The margin boundaries where support vectors lie.</td>
  </tr>
  <tr>
    <td><b>Equation</b></td>
    <td>w &bull; x + b = 0</td>
    <td>w &bull; x + b = +1 and w &bull; x + b = -1</td>
  </tr>
  <tr>
    <td><b>Purpose</b></td>
    <td>Divides the feature space into two halves.</td>
    <td>Defines the extent of separation for the classes.</td>
  </tr>
  <tr>
    <td><b>Location</b></td>
    <td>Lies exactly between the two decision boundaries.</td>
    <td>Lies at the edge of the margins.</td>
  </tr>
</table>
<br>

<li><b>Margin:</b> The margin is the distance between the hyperplane and the closest data points (called support vectors) from either class.<br>
SVM aims to maximize this margin to ensure the model generalizes well.</li><br>

<li><b>Support Vectors:</b> These are the data points closest to the hyperplane and influence its position and orientation.<br>
Only these points are relevant in defining the hyperplane.</li><br>

<li><b>Kernel Trick:</b> SVM can handle non-linearly separable data by transforming the original input space into a higher-dimensional feature space using 
kernel functions. The choice of kernel significantly affects the SVM's performance and the complexity of the decision boundary. Popular kernel functions include:
  <br><br>
  
  <ol type='1'>
<li><b>Linear Kernel:</b> The linear kernel is the simplest kernel function. It computes the dot product between two vectors in the original feature space.<br>
K(x, y) = x &bull; y<br><br>
Characteristics:
  <ul>
<li>Suitable for linearly separable data (where a straight line or hyperplane can separate the classes).</li>
<li>The decision boundary is a linear function.</li>
<li>Computationally efficient because no transformation is performed.</li>
  </ul>
  
Use Case:
  <ul>
<li>When the data is already linearly separable.</li>
<li>For high-dimensional datasets where linear separation is likely.</li></li>
  </ul>
  <br>

<li><b>Polynomial Kernel:</b> The polynomial kernel allows for more complex decision boundaries by computing the dot product raised to a power d, along with 
  optional coefficients.<br>
  K(x, y) = (𝛾x &bull; y + r)<sup>d</sup> where:<br><br>
    d: Degree of the polynomial (controls complexity of the model).<br>
    γ: A scaling factor for the input data (default is usually 1/n<sub>features</sub>)<br>
    r: A coefficient that shifts the function (default is often 0).<br><br>
    Example: For d=2 (quadratic kernel), it can model circular or elliptical decision boundaries.<br>
    
Characteristics:<br>
<ul>
<li>Captures interactions of features up to the d-th degree.</li>
<li>Produces a non-linear decision boundary.</li>
<li>More flexible than the linear kernel but computationally more expensive.</li>
  </ul>
  
Use Case:<br>
<ul>
<li>When the relationship between the features and the target is non-linear and can be captured by polynomial interactions.</li>
<li>For moderately complex datasets.</li>
  </ul></li>
  <br>
  
<li><b>Radial Basis Function (RBF) or Gaussian Kernel:</b> The RBF kernel maps the data into an infinite-dimensional feature space using a Gaussian function. 
  It measures similarity based on the distance between two points.<br>
  K(x, y) = exp(-γ ||x - y||<sup>2</sup>) where, γ: Kernel coefficient (controls the influence of each training example).<br>
  
Characteristics:<br>
<ul>
<li>Highly flexible and can model very complex decision boundaries.</li>
<li>Effective for datasets with non-linear relationships.</li>
<li>The parameter γ controls the "spread" of the Gaussian function:<br>
  <ul>
<li>High γ: Focuses on closer points, leading to tighter decision boundaries (risk of overfitting).</li>
<li>Low γ: Considers distant points, leading to smoother boundaries (risk of underfitting).</li></li>
  </ul></ul>
  <br>
  
Use Case:<br>
<ul>
<li>When the data is not linearly separable.</li>
<li>For datasets with complex, non-linear patterns.</li>
</ul>
</li></li>
  </ol>
  <br>

<table border="1" style="border-collapse: collapse; width: 100%; text-align: left;">
  <caption><b>Comparison of Kernel Functions</b></caption>
  <tr>
    <th>Kernel</th>
    <th>Definition</th>
    <th>Decision Boundary</th>
    <th>Use Case</th>
    <th>Kernel Equation</th>
    <th>Pros</th>
    <th>Cons</th>
  </tr>
  <tr>
    <td>Linear</td>
    <td>Used for linearly separable data.</td>
    <td>Linear</td>
    <td>Linearly separable data.</td>
    <td>K(x<sub>i</sub>, x<sub>j</sub>) = x<sub>i</sub> &bull; x<sub>j</sub></td>
    <td>Simple, fast, interpretable.</td>
    <td>Poor for non-linear data.</td>
  </tr>
  <tr>
    <td>Polynomial</td>
    <td>Maps input into higher-dimensional polynomial space.</td>
    <td>Non-linear (polynomial)</td>
    <td>Non-linear data with polynomial relationships.</td>
    <td>K(x<sub>i</sub>, x<sub>j</sub>) = (γx<sub>i</sub> &bull; x<sub>j</sub> + r)<sup>d</sup></td>
    <td>Captures feature interactions.</td>
    <td>Higher degree can overfit.</td>
  </tr>
  <tr>
    <td>RBF (Gaussian)</td>
    <td>Maps input to infinite-dimensional space based on similarity.</td>
    <td>Highly non linear</td>
    <td>Non-linearly separable data.</td>
    <td>K(x<sub>i</sub>, x<sub>j</sub>) = exp(-γ||x<sub>i</sub> - x<sub>j</sub>||<sup>2</sup>)</td>
    <td>Very flexible, powerful for complex data.</td>
    <td>Sensitive to hyperparameters.</td>
  </tr>
</table>
</ul>
<br>

<h3><b>Mathematical Objective</b></h3> The main aim is to minimize:<br>
(1/2).∥w∥<sup>2</sup>, where w = sqrt(w<sub>1</sub><sup>2</sup> + w<sub>2</sub><sup>2</sup>)<br><br>

SVM optimization can also be solved in its dual form using Lagrange multipliers, which is computationally efficient for high-dimensional data.<br>
We find suitable parameters for the hyperplane and can plot the hyperplane to distinguish data points.

<h3><b>Applications</b></h3>
<ul>
<li>Classification: Text classification (e.g., spam detection), Image recognition.</li>
<li>Regression: Predict continuous values using Support Vector Regression (SVR).
<li>Outlier Detection: Anomaly detection in fraud detection and intrusion systems.</li>
</ul>

<h3><b>Support Vector Classifier (SVC)</b></h3>
SVC is a supervised machine learning algorithm based on Support Vector Machines (SVM). It is widely used for binary classification and can be extended for multiclass classification using specific strategies.

<ul>
<li><h4><b>Binary Classification with SVC</b></h4> 
In binary classification, SVC separates data into two classes using a hyperplane in the feature space. It attempts to find the optimal hyperplane that maximizes the margin between the two classes.<br><br>

Equation of the hyperplane: w⋅x+b=0<br><br>
Decision boundaries:<br>
w⋅x+b=+1 (support vectors for class 1)<br>
w⋅x+b=−1 (support vectors for class 2)<br>

Steps
<ul>
<li>Compute support vectors that are closest to the decision boundary.</li>
<li>Find the hyperplane that maximizes the margin while ensuring correct classification of all training points.</li>
</ul>
<br>

Key Features
<ul>
<li>Works well for linearly separable data.</li>
<li>Can handle non-linear data using kernel functions (e.g., polynomial, RBF).</li>
</ul>
</li>
<br>

<li><h4><b>Multiclass Classification with SVC</b></h4>
SVM inherently supports only binary classification. For multiclass classification, SVC uses strategies like One-vs-One (OvO) or One-vs-Rest (OvR) to extend its capability.<br>

<b>One-vs-One (OvO) Strategy:</b> SVC in scikit-learn handles multi-class classification by default using the one-vs-one (OvO) approach.<br>
OvO creates a binary classifier for every pair of classes. For n_classes, there are <sup>n</sup>C<sub>2</sub> classifiers trained.<br>
The final prediction is made by voting: the class that wins the most pairwise comparisons is assigned as the prediction.<br>

<b>One-vs-Rest (OvR) Strategy:</b> Trains n classifiers, one for each class versus the rest of the classes combined.<br>
Chooses the class with the highest confidence score. Faster than OvO for larger datasets.

<h2><b>Note:</b></h2> Decision Boundaries in Multi-Class: In multi-class datasets, SVC creates boundaries that separate each class from the others. These boundaries may be linear (for kernel='linear') or non-linear (for kernel='rbf' or poly).


</li>
</ul>

