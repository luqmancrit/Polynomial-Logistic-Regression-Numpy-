# Polynomial Logistic Regression: Simple, Small, Numpy
Implementation of logistic regression model using polynomial feature mapping. It is designed to be easy to use and modify, with functions for feature mapping, optimization, and evaluation. The code is well-documented and focused on simplicity and efficiency, making it a useful resource for anyone interested in logistic regression models with Numpy.

<img src="https://github.com/luqmancrit/Polynomial-Logistic-Regression-Numpy-/blob/main/images/dev%20set%20-%20loss%20value.png?raw=true" alt="alt text" width="1200" height="300">

## Data Acquisition
1. The data can be obtained from a source like Kaggle.
Note: EDA is not performed. The data is already clean.

## Data Preprocessing
1. The data has be scaled down to ensure that features are on similar scales and to prevent any one feature from dominating the model.
2. Map the features using a technique like polynomial feature mapping, which allows for more complex relationships between features and the target variable.

## Data Splitting
1. Split the data into training, dev, and test sets. The training set is used to train the model, the dev set is used to tune hyperparameters and evaluate the model's performance, and the test set is used to assess the final performance of the model.

## Model Training
1. Set a desired level of accuracy for the model and initialize the parameters for the training set.
2. Run diagnostic tests to identify any overfitting or underfitting and adjust the model to improve performance on the dev set until the desired accuracy is achieved.

## Model Evaluation
1. Choose the model with the best balance between overfitting and underfitting by evaluating its performance on the dev set.
2. Finally, use the test set to evaluate the final performance of the chosen model and confirm that it is generalizable to new data.
