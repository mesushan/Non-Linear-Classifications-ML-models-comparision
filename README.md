# Non-Linear-Classifications-ML-models-comparision

Using Näive Bayes, Decision Tree and Random Forest on same dataset and comparing the model prediction

## Problem

Suppose a company is going to launch a new campaign for their new brand of SUV and want to know which category of people are likely to buy their brand new SUV so they can have the ads that target those peoples. For this they contacted a social network advertising company which have the data from another similar successful campaign. Now, they want to make a model which helps achieve their goal.

## Dataset

The dataset contains 400 entries which contains the userId, gender, age, estimatedsalary and the purchased history. The matrix of features taken into account are age and estimated salary which are going to predict if the user is going to buy new SUV or not(1=Yes, 0=No).

## Solution

First the pre-processing of data is done and then the prediction is done using three non-linear classifiers (Naive Bayes Classification, Decision Tree Classification and Random Forest classification). The confusion matrix and visualization clearly shows the prediction made by all three models and the best model for this dataset. The dataset is split into 75/25 ratio (training set = 0.75 & test set = 0.25).

The confusion matrix with Naive Bayes classifier shows that our model predicts 90 correct and 10 wrong decisions which shows 90% accuracy.

![cm_naive_bayes](https://user-images.githubusercontent.com/14214659/71474531-97248080-27e4-11ea-8699-e0637830ff83.png)

The confusion matrix with Decision Tree classifier shows that our model predicts 91 correct and 9 wrong decisions which shows 91% accuracy.

![cm_decision_tree](https://user-images.githubusercontent.com/14214659/71474554-adcad780-27e4-11ea-8e5f-97756f5c3bc2.png)

The confusion matrix with Random Forest classifier (with 10 trees) shows that the model predicts 91 correct and 9 wrong decisions which shows 91% accuracy.

![cm_random_forest](https://user-images.githubusercontent.com/14214659/71474569-c5a25b80-27e4-11ea-99d0-2ad008980e0e.png)

The data visualization of the training set and test set is given below. As all the models are non-linear, the graph is non-linear. The green dots shows the people buying the car whereas red dots shows the people not buying the car. The green dots on the green region shows the true positive whereas the red dots on the red region shows the true negative. The wrongly classified are the green dots in the red region (false negative) and the red dots in the green region (false positive).

![Naive Bayes (Training set)](https://user-images.githubusercontent.com/14214659/71476457-e1f6c600-27ed-11ea-8517-6e2dd12498dd.png)

![Naive Bayes (Test set)](https://user-images.githubusercontent.com/14214659/71476466-ee7b1e80-27ed-11ea-8ae0-243e6f7a099b.png)

![Decision Tree ( Training set)](https://user-images.githubusercontent.com/14214659/71476478-fb980d80-27ed-11ea-8a2d-b38dfaca85a2.png)

![Decision Tree (Test set)](https://user-images.githubusercontent.com/14214659/71476488-06eb3900-27ee-11ea-96e0-4a212c819072.png)

![RF Classification (Training set)](https://user-images.githubusercontent.com/14214659/71476504-1074a100-27ee-11ea-86bd-81ebd0e73b64.png)

![RF  Classification (Test set)](https://user-images.githubusercontent.com/14214659/71476519-1c606300-27ee-11ea-8f14-f04136ca4bd9.png)

## Conclusion

From the confusion matrix, it looks like DT and RF is the best model for this data as they both have 91% accuracy compared with Naive Bayes but if we analyze the graph, the story is different. The naive bayes graph is smooth and catches most of the original values whereas in RF and DT, it looks like there is over-fitting as the model tries to catch all the correct prediction and the graph shows that there are some space with empty values meaning it is over-fitting the data. From this interpretation, we can conclude that for this particular dataset naive bayes classifier is the best one.
