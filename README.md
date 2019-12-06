# Udacity-Capstone-Sparkify

## Capstone Project, Udacity Data Science Nanodegree

Medium.com : https://medium.com/@mohlat88/udacity-capstone-project-sparkify-470263836e3c?sk=d684c6d25ec1c5569d075c8cc2a97360

## Files Contained in this Repo
1. Sparkify.ipynb
2. Readme.md

## Overview:
Sparkify is a music app. The log data provided contains some basic information about the user as well as information about a single action. A user can contain many entries. In the data, a part of the user is churned, through the cancellation of the account behavior can be distinguished.

## Data
User log used from Udacity workspace

## Packages:
PySpark, Pandas, Seaborn, Matplotlot.pylpot

## Models:
Logistic Regression, Decision Tree Classifier, GBT Classifier

1. Project Overview
2. Problem Statement
3. Data Preprocessing
4. Metrics
5. Feature Engineering
6. Modelling
7. Results

## Results:
The result is not ideal, the recall rate of the model is very low, even the recall rate of the tree model is 0. I decided to undersample the training data, balance the categories of the training set to increase the recall rate and improve f1.
There is a strange problem here. Training results through cross-validation is good, but testing with validation sets is very poor. Logistic regression for example, the training result F1 score is 0.75, and the test result F1 score is 0.4. After the use of undersampling, the training result drops to 0.67, and the test result is 0.55.
Training: 0.758073899263998
Testing: 0.4
Training with undersample: 0.6696185966538797
Testing with undersample: 0.5517241379310345
The best model is logistic regression. According to the results of the model, it is the frequency of Thumbs Down that has the greatest impact. Churn users have more Thumbs Down. Naturally, users will leave if they are not satisfied.
Besides, the frequency of downgrade pages is also a big factor. I think this is because users hate the downgrade prompt. Registration time is also a factor, the longer the registration time users will not leave.

This is mostly a practice of using spark environment to analyze large volume of data, the main part can be replicated locally by just using packages like panads and numpy.
