---
layout: post
title:      "Solving a Classification Problem in Machine Learning "
date:       2019-02-26 19:21:36 -0500
permalink:  solving_a_classification_problem_in_machine_learning
---


For project No.3 we were asked to select a data set of our choice to create a classification model. I choose the census data set from the UCI Machine Learning Repository; the target for this project was to train a binary classifier to predict income greater than 50K or less than 50K based on data from the 1996 US census. 

Classification is a core problem in Machine Learning and the goal is to teach computers by example, it answers to yes/no questions; so we used data from the past to predict the future; in this case we want to be able to predict income based on attributes like age, sex, education level, race, relationship status, and occupation among others. 

The first thing I did was feature engineering, this is an iterative process to explore and understand the data relationships, good features allow simple machine learning algorithms to work well, so spending some quality time in this step will be rewarded when modeling.  I performed numeric transformation to categorical features (label encoding), looked at the descriptive statistics, normalization, and made visualization plots of demographical data and the target variable (income). 

For this project I compared two algorithms, Logistic Regression and XGBoost, part of the ensemble methods-.
Logistic Regression minimizes the average loss on the training points, it uses a sigmoid function, which acts as a binary classifier, and the model evaluates on some combination of precision, recall and accuracy. XGBoost is a stand-alone library that implements popular gradient boosting algorithms at a fast and high level of efficiency.
My LR model worked well for incomes (of or less than) 50K, for incomes greater than 50K the F1 Score was really low which meant the model did not do well for this part of the target. Based on the confusion matrix for this model, the misclassification rate was 20.76% 
For the XGBoost classifier, the most important features were age, capital gain, education and capital loss; it performed better than the previous model with only 13.8%. 
To answer the initial question, Can we predict and classify income based on the questions asked in the census? Yes we can predict income with a comfortable level of accuracy in the predictions. 

Given more time I would have trained more models to compare the results. This project was a good practice to get into supervised learning and how to apply different models. 
