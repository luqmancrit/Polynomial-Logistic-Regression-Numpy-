# 🎛️Polynomial Logistic Regression: Regularized, Small, Numpy
Hi and welcome! This project is an implementation of logistic regression model using polynomial feature mapping. The modeling process involved simple processing, diagnostics, and testing approach. The objective is to build a model to predict userbase purchasing decision, using small dataset (400) and Numpy.<br>

<img src="https://github.com/luqmancrit/Polynomial-Logistic-Regression-Numpy-/blob/main/images/dev%20set%20-%20loss%20value.png?raw=true" alt="alt text" width="1200" height="350">

## 📑Motivation
Business competition is getting crowder every day. Businesses needs to keep striving and be profitable. Understanding and collecting data of demographics of interested buyer from userbase is such a crucial step. It is also crucial for companies to take advantage of the collected data, to understand the pattern of the buying customers.<br>

By building a model to predict userbase purchase, will lead the company to have future advantages of:<br>
- Precise financial decision.
- Targeted marketing.
- Stay competitive and lasts.<br>

Further step of processing, training, and evaluation the model will be explained further below.

## 📋Data Acquisition
The data can be obtained from a source like Kaggle.<br>

<img src="https://github.com/luqmancrit/Polynomial-Logistic-Regression-Numpy-/blob/main/images/dataset.png?raw=true" alt="alt text" width="400" height="250">

## 🔎Data Preprocessing
1. The feature has high scale difference, so the data has be scaled down to ensure that features are on similar scales and to prevent any one feature from dominating the model.
2. The dataset clearly shows the decision boundary is polynomial. Polynomial feature mapping technique be used, which allows for more complex relationships between features and the target variable.

## 🔃Data Splitting
To ensure the model is generalized well and not overfitting, the data will be splitted into three different sets:<br>
- Training set - 60%
- Development set - 20%
- Test set - 20%

Splitting the data will lead to a faster process of finding the optimal predicition model, since time is a limited source. 

## 🏂Model Training
A benchmark for desired metrics and initial parameters has been set earlier for further process:

Success metrics:
- Model accuracy: 90-95%.
- Accuracy gap: 2-3%

Initial Parameters:
- Alpha: 0.01
- Lambda regularized: 0.1
- Iterations: 1000
- Degree polynomial: 1, 2, 3, 4, 5, 6

Result Obtained:<br>
- Degree that possible generalizes: 2, 3 
- Training set accuracy:
  - Degree 2: 87.92%
  - Degree 3: 85.83%
- Desired model accuracy: Not desired.

<img src="https://github.com/luqmancrit/Polynomial-Logistic-Regression-Numpy-/blob/main/images/train%20set%20-%20loss%20values.png?raw=true" alt="alt text" width="600" height="250">

## 🎿Model Evaluation
The desired model accuracy is not achieved during training set. The model will be proceed to be evaluated using different feature and metrics:

- Dataset: Development set (20%)
- Polynomial degree: 2, 3
- Lambda regularized: 0.1, 1
- Iterations: 1000
- Alpha: 0.01

Result: The initial benchmark passed! Model with degree: 2, lambda regularized: 1 accuracy is: 90% 

<img src="https://github.com/luqmancrit/Polynomial-Logistic-Regression-Numpy-/blob/main/images/dev%20set%20-%20loss%20value.png?raw=true" alt="alt text" width="1200" height="350">

## 🎯Model Testing
Overfitting model diagnostics be performed afterwards using test set, to choose a model that generalized well to new data.<br>
Result: 
- Test set model accuracy: 95%. 
- Accuracy gap: +5%

Observation: The test model is generalizing well to new, unseen data, which is the ultimate goal of this prediction model.

## 🪂Conclusion
As a conclusion, the best generalized well model to predict user purchasing behaviour with accuracy gap: +5% has been achieved successfully.
