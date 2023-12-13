# Machine Learning Interview Questions & Answers

### Q1 -What are the Bias and Variance in a Machine Learning Model and explain the bias-variance trade-off?
Bias and variance are two fundamental sources of error in machine learning models. Understanding these concepts is crucial for assessing and improving model performance.

Bias: It is the error introduced by approximating a real-world problem, which may be extremely complex, by a simplified model. It measures how far off our predictions are from the actual values.
Characteristics:
High bias indicates that the model is too simple and fails to capture the underlying patterns in the data.
Models with high bias are often oversimplified and tend to underfit the data.
Example:
A linear regression model applied to a non-linear dataset will likely have high bias.

Variance: It is the amount by which our model's predictions would change if we trained it on a different dataset. It measures the model's sensitivity to the fluctuations in the training data.
Characteristics:
High variance indicates that the model is too complex and is capturing noise in the training data.
Models with high variance are often too flexible and tend to overfit the data.
Example:
A high-degree polynomial regression model applied to a small dataset may have high variance.
Bias-Variance Trade-off:
The bias-variance trade-off is a fundamental concept in machine learning, representing the balance between a model's ability to capture the underlying patterns in the data (low bias) and its sensitivity to noise and fluctuations (low variance). The goal is to find the optimal level of model complexity that minimizes both bias and variance, ultimately leading to better generalization performance on unseen data.
