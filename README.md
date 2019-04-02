# ML-Learning

This repository includes common questions and relevant materials on different topics of machine learning algorithms.

## Logistic Regression

### Is logistic regression a linear or a non-linear model ?
Logistic regression is considered a linear model as the decision boundary would be a linear function of x i.e. the predictions can be written as linear combination of x.

if p=1/(1+ e^(-z)) and if p=0.5 is the threshold then z=0 is the decision boundary.
[link1](https://stats.stackexchange.com/questions/93569/why-is-logistic-regression-a-linear-classifier)
[link2](https://www.quora.com/Why-is-logistic-regression-considered-a-linear-model)


### Why can't we use the cost function of Linear Regression in Logistic Regression?
If we try to use the cost function of the linear regression in ‘Logistic Regression’ then it would be of no use as it would end up being a non-convex function with many local minimums, in which it would be very difficult to minimize the cost value and find the global minimum. So we define the log cost function for logistic regression which is quite convex in nature.
Below is short explaination for it.
"In case y=1, the output (i.e. the cost to pay) approaches to 0 as y_pred approaches to 1. Conversely, the cost to pay grows to infinity as y_pred approaches to 0. This is a desirable property: we want a bigger penalty as the algorithm predicts something far away from the actual value. If the label is y=1 but the algorithm predicts y_pred=0, the outcome is completely wrong."
[link1](https://www.internalpointers.com/post/cost-function-logistic-regression)
[link2](https://towardsdatascience.com/introduction-to-logistic-regression-66248243c148)

### Can Logistic Regression be used for multiclass classification ?
Yes, using one-vs-all classification. Suppose there are 3 different classes we want to predict. We would train 3 different classifiers for each class i to predict the probability that y=i and then finally take the class that has the max probabilty while prediction.


### Is standardization required in logistic regression?
Standardization isn't required for logistic regression. The main goal of standardizing features is to help convergence of the technique used for optimization. It's just that standardizing the features makes the convergence faster.


### AIC ?
[link](https://www.methodology.psu.edu/resources/aic-vs-bic/)

### What is L1(Ridge), L2(LASSO) regularization ?
Regularization is a technique to discourage the complexity of the model. It does this by penalizing the loss function. This helps to solve the overfitting problem.
In L1 regularization we change the loss function to this:

L1 regularization does feature selection. It does this by assigning insignificant input features with zero weight and useful features with a non zero weight.

L2 regularization forces the weights to be small but does not make them zero and does non sparse solution. L2 is not robust to outliers as square terms blows up the error differences of the outliers and the regularization term tries to fix it by penalizing the weights.

[link](https://medium.com/datadriveninvestor/l1-l2-regularization-7f1b4fe948f2)
