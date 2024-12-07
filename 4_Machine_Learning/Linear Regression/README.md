<h2><b>Linear Model Regression</b></h2>
Linear Model Regression refers to a type of regression analysis that models the relationship between one or more independent variables (predictors) and a dependent 
variable (outcome) using a straight line (in case of one predictor) or a hyperplane (in case of multiple predictors). The key assumption is that the dependent 
variable is a linear function of the independent variables. (Sometimes polynomial function is also used)<br><br>

Key Objectives of Linear Regression:
<ul>
<li>Understand Relationships: It determines how changes in the independent variables affect the dependent variable.<br>
Example: How does a person's age and income affect their spending?</li>
  
<li>Make Predictions: Use the model to predict the dependent variable for new input data.<br>
Example: Predict house prices based on square footage and location.</li>
</ul>

Types of Linear Regression:<br>
<ol type='1'>
<li><b>Simple Linear Regression:</b> Models the relationship as a straight line:<br>
y=mX+b, where m:coef_ and b:intercept_<br>
Example: Predict a person's height based on their age.</li><br>
  
<li><b>Multiple Linear Regression:</b> Models a target variable based on multiple independent variables:<br>
𝑦=𝛽<sub>0</sub> + 𝛽<sub>1</sub>𝑋<sub>1</sub> + ... + 𝛽<sub>n</sub>X<sub>n</sub>, where 𝛽<sub>1</sub>,...., 𝛽<sub>n</sub>:coeff_ and  𝛽<sub>0</sub>:intercept_<br>
Example: Predict car price based on mileage, age, and brand.</li><br>

<li><b>Polynomial Regression:</b> Fits a non-linear relationship by transforming features into polynomial terms:<br>
𝑦=𝛽<sub>0</sub> + 𝛽<sub>1</sub>𝑋 + 𝛽<sub>2</sub>X<sup>2</sup> + ... + 𝛽<sub>n</sub>X<sup>n</sup><br>
Example: Population growth might follow a polynomial pattern due to varying birth rates, migration, and other factors.</li>
</ol>
