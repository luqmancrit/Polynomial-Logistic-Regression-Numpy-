# 🎛️Polynomial Logistic Regression: Regularized, Small, Numpy
Hi and welcome! This project is an implementation of logistic regression model using polynomial feature mapping. The modeling process involved simple processing, diagnosting, and testing approach. The objective is to build a model to predict userbase purchasing decision, using small dataset (400) and Numpy.<br>

<img src="https://github.com/luqmancrit/Polynomial-Logistic-Regression-Numpy-/blob/main/images/multi%20degree%20decision%20boundary.png?raw=true" alt="alt text" width="600" height="250">

## 🔮General Modeling Process
Below is the general modeling process that will be discussed in this project. Further step of processing, training, and evaluation the model will be explained below.<br>

<img src="https://github.com/luqmancrit/Polynomial-Logistic-Regression-Numpy-/blob/main/images/general%20modeling.png?raw=true" alt="alt text" width="600" height="250">

## 📑Motivation
Business competition is getting crowder every day. Businesses needs to keep striving and be profitable. It is crucial for companies to take advantage of the collected data, to understand the pattern of the buying customers.<br>

By building a model to predict userbase purchase, will lead the company to have future advantages of:<br>
- Precise financial decision.
- Targeted marketing.
- Stay competitive and lasts.<br>

## 📋Data Acquisition
The data can be obtained from a source like Kaggle.<br>

<img src="https://github.com/luqmancrit/Polynomial-Logistic-Regression-Numpy-/blob/main/images/dataset.png?raw=true" alt="alt text" width="400" height="250">

## 🔎Data Preprocessing
- Feature scaling: The feature has high scale difference, so the data has be scaled down to ensure that features are on similar scales and to prevent any one feature from dominating the model.
- Feature mapping: The dataset clearly shows the decision boundary is polynomial. Polynomial feature mapping technique be used, which allows for more complex relationships between features and the target variable.

## 🔃Data Splitting
To ensure the model is generalized well and not overfittingthe data will be splitted into fraction of sets. Splitting the data will lead to a faster process of finding the optimal predicition model, since time is a limited source. Three different sets:<br>
- Training set=60%
- Development set=20%
- Test set=20% 

## 🎿Model Development
### Polynomial Degree
The dataset clearly shows that the decision boundary is non-linear. The degree value to be choose are identified to prevent overfitting model. Below is the earlier finding degree value for decision boundary.

Result: Degree 2, 3 seems generalized well. Further process will be proceeded using degree: 2, 3.

<img src="https://github.com/luqmancrit/Polynomial-Logistic-Regression-Numpy-/blob/main/images/multi%20degree%20decision%20boundary.png?raw=true" alt="alt text" width="600" height="250">

### 🏂Model Training
A benchmark for desired metrics and initial parameters has been set earlier for further process:

Success metrics:
- Model accuracy=90-95%.
- Accuracy gap=2-3%

Initial Parameters:
- Alpha: 0.01
- Lambda regularized: 0.1
- Iterations: 1000
- Degree polynomial: 1, 2, 3, 4, 5, 6

Result:<br>
- Degree that possible generalizes: 2, 3 
- Training set accuracy:
  - Degree 2: 87.92%
  - Degree 3: 85.83%
- Desired model accuracy: Not desired.

<img src="https://github.com/luqmancrit/Polynomial-Logistic-Regression-Numpy-/blob/main/images/train%20set%20-%20loss%20values.png?raw=true" alt="alt text" width="600" height="250">

### 🛼Model Evaluation
The desired model accuracy is not achieved during training set. The model will be proceed to be evaluated using different feature and metrics:

- Dataset: Development set (20%)
- Polynomial degree: 2, 3
- Lambda regularized: 0.1, 1
- Iterations: 1000
- Alpha: 0.01

Result: 
Model accuracy (degree: 2, lambda regularized 1)=90%

Observation: Desired model accuracy has achieved!

<img src="https://github.com/luqmancrit/Polynomial-Logistic-Regression-Numpy-/blob/main/images/dev%20set%20-%20loss%20value.png?raw=true" alt="alt text" width="1200" height="350">

### 🎯Model Testing
Result:
- Model accuracy: train=88%, dev=90%, test=95%
- Accuracy gap: +5%

Observation:
- The model accuracy on the test set (95%) meets the benchmark for high accuracy. But the accuracy gap between the development and test sets is 5%, which is higher than the desired range of 2-3%.
- Development model cross training model at iteration 500.
- Desired model accuracy: Yes<br>
- Desired accuracy gap: No<br>

Further development: Fine-tuning.

<img src="https://github.com/luqmancrit/Polynomial-Logistic-Regression-Numpy-/blob/main/images/test%20set%20accuracy%201.png?raw=true" alt="alt text" width="500" height="150">

## 🎚️Fine-tuning
The fine-tuning process be performed to change hyperparameters, to achieve the desired metrics Hyperparameters to be change are:
- Lambda regularized: 0.1,0.2,0.4,0.8,1
- Iteration: 500

Result:
- Development model with degree 2 with all lambda regularized values, has highest accuracy=91.25%.
- Loss value model with degree 2, lambda regularized 1 development model lies on training model uncrossed.

Observation: 
- Model with degree 2 and lambda regularized 1 perform the best.
- Fine-tuned development model pass the desired accuracy and higher than previous development accuracy!

<img src="https://github.com/luqmancrit/Polynomial-Logistic-Regression-Numpy-/blob/main/images/fine%20tuning%20loss%20value.png?raw=true" alt="alt text" width="1200" height="350">

## 🧬Fine-tuning testing
Result:
- Fine-tuned test set accuracy=93.75%
- Accuracy gap=+2%

Observation: 
- Desired model accuracy and gap accuracy passed! 
- The model generalized well with unseen data which make it a great prediction model.

<img src="https://github.com/luqmancrit/Polynomial-Logistic-Regression-Numpy-/blob/main/images/fine%20tuning%20test%20model%20accuracy.png?raw=true" alt="alt text" width="500" height="150">

## 🪂Conclusion
Model Accuracy & Performance Recap:
- Model Training:
  - Training set (degree=3)=87.50%
  - Training set (degree=2)=86.67%

- Model Development:
  - Development set=90%
  - Test set=95%
  - Accuracy gap=+5%
  - Desired metrics=No

- Fine-tuning:
  - Development set (degree=2, lambda=1)=91.25%
  - Test set=93.75%
  - Accuracy gap=+2%
  - Desired metrics=Yes
  
As a conclusion, the user purchase predicition model go through development and fine-tuning process to find the model that generalized well. Finally, the best generalized well model to predict user purchasing behaviour with model accuracy of 93.75%, and accuracy gap: +2% has been achieved successfully.
