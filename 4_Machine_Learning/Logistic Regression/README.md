<h2><b>Logistic Regression</b></h2>
Logistic Regression is a statistical method used for classification and, more broadly, for predicting categorical outcomes. It is widely used in machine learning when
the target variable represents categories or classes.<br>
Predicts a probability that a given input belongs to a particular class.<br>
Commonly used for binary classification (two classes, e.g., yes/no, spam/ham).<br><br>

Types:<br>
<ol type='1'>
  <li><b>Binary Classification:</b> For binary classification, the goal is to predict one of two possible classes (e.g., y∈{0,1}). It uses the sigmoid function to map
    predictions to probabilities between 0 and 1.<br>
    Example: Spam detection: Is an email spam or not?<br>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Loan approval: Will a person default on a loan?
    
  ![image](https://github.com/user-attachments/assets/3adab001-abc9-42d1-9cad-7c15e4202cd1)

  Equation for Binary Classification:<br><br>
  ![image](https://github.com/user-attachments/assets/677ce820-90b2-4fc8-a252-29a4f3bb987c)

  where, model.coef_ (W) determines the slope of the sigmoid curve and model.intercept_ (b) shifts the sigmoid curve horizontally.<br><br>
  <b>Note:</b> The threhold is generally 0.5.
</li><br>

<li><b>Multiclass Classification:</b> For multiclass classification (e.g., y∈{0,1,2,…,K−1} where K is the number of classes), the goal is to predict one of K possible
  classes.<br>
Example: Predicting which category a product belongs to.<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Classifying types of flowers.<br>

The probabilities for all classes are modeled using the softmax function, which generalizes the sigmoid function to multiple classes:<br>
![image](https://github.com/user-attachments/assets/c0a02b87-6200-4b30-b7f2-02605e98cc3e)<br>
![image](https://github.com/user-attachments/assets/cecd4d3e-4833-4af3-bec9-458f9c1c63ad)<br>
![image](https://github.com/user-attachments/assets/a1fa53c9-933a-4821-9ea7-efe36c7958a2)<br><br>

<b>Note:</b> Threshold in Multiclass Classification:<br>
The softmax function is used to compute probabilities for all classes. Each observation gets a vector of probabilities, one for each class. The predicted class is 
typically the one with the highest probability. This effectively uses a single threshold of "maximum probability."<br>
Example:<br>
![image](https://github.com/user-attachments/assets/d76de6c6-bd54-4706-a3d1-e80605848e5c)







</li>
</ol>
