## Ridge and Lasso regression-
Ridge and Lasso regression are powerful techniques generally used for creating parsimonious models in presence of a ‘large’ number of features. Here ‘large’ can typically mean either of two things:
* Large enough to enhance the tendency of a model to overfit (as low as 10 variables might cause overfitting)
* Large enough to cause computational challenges. With modern systems, this situation might arise in case of millions or billions of features
<br></br>Though Ridge and Lasso might appear to work towards a common goal, the inherent properties and practical use cases differ substantially. If you’ve heard of them before, you must know that they work by penalizing the magnitude of coefficients of features along with minimizing the error between predicted and actual observations. These are called ‘regularization’ techniques. The key difference is in how they assign penalty to the coefficients:

* Ridge Regression:
  * Performs L2 regularization, i.e. adds penalty equivalent to square of the magnitude of coefficients
  * Minimization objective = LS Obj + α * (sum of square of coefficients)
* Lasso Regression:
  * Performs L1 regularization, i.e. adds penalty equivalent to absolute value of the magnitude of coefficients
  * Minimization objective = LS Obj + α * (sum of absolute value of coefficients)
Note that here ‘LS Obj’ refers to ‘least squares objective’, i.e. the linear regression objective without regularization.

If terms like ‘penalty’ and ‘regularization’ seem very unfamiliar to you, don’t worry we’ll talk about these in more detail through the course of this article. Before digging further into how they work, lets try to get some intuition into why penalizing the magnitude of coefficients should work in the first place.
