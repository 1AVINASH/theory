## Loss function
* A mathematical function that measures the discrepancy between a model's predicted output and the actual target values
* The goal is to minimise the loss function during model training
* Loss focuses on the distance between the values, not the direction. For example, if a model predicts 2, but the actual value is 5, we don't care that the loss is negative. Instead, we care that the distance between the values is.

## Linear Regression
* y = b + w1x1 (same as y = mx + c)
* Here y is the predicted label of the model. b is the bias (same as m), and w1 is the weight of the parameter. x1 is the value of the feature

## RMSE (Root Mean Squared Error)
Root Mean Squared Error (RMSE) is a widely used metric in machine learning to evaluate the performance of regression models. It measures the average magnitude of the errors between predicted and actual values, giving more weight to larger errors. 

## Decision Tree Regression
Decision tree regression is a supervised machine learning technique used to predict continuous numerical values. It creates a tree-like model where each node represents a decision rule on a feature, leading to leaf nodes that provide predicted values. The algorithm splits the data into subsets based on features that minimize prediction error, forming a tree structure that captures non-linear relationships in the data. 
    * A decision tree regression model is built by recursively partitioning the data based on features.
    * Each internal node represents a decision rule on a feature, splitting the data into subsets.
    * Each branch represents the outcome of a decision, leading to a new node.
    * Leaf nodes contain the predicted values, which are often the average of the target values within that subset.

## Logistic regression
* Logistic regression is an extremely efficient mechanism for calculating probabilities
* A statistical method used for binary classification, meaning it predicts one of two outcomes (e.g., yes/no, pass/fail) based on a set of input variables. 
* It determines the probability of a specific event occurring, often using a sigmoid function to map input values to a probability between 0 and 1. 
* It uses a sigmoid curve