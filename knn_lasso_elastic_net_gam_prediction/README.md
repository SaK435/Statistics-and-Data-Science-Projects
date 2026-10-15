# KNN vs Lasso Logistic Regression, and Elastic Net vs GAM

This folder contains R code from two supervised learning projects. All code is in
one R Markdown file: `knn_lasso_elastic_net_gam.Rmd`

## Part A: KNN vs Lasso logistic regression (bias variance trade off)

Goal: compare a K nearest neighbours classifier with lasso logistic regression
on a simulated binary classification data set (10000 cases, 3 relevant
predictors and 200 irrelevant noise predictors), and explain the results with
the bias variance trade off.

Approach:
* First 5000 cases as training data, next 5000 as test data
* Two settings: only 3 relevant plus 3 irrelevant predictors, and all 203
  predictors
* K for KNN chosen with 10 fold cross validation (predictors centred and scaled)
* Lambda for lasso logistic regression chosen with 10 fold cross validation
* Accuracy on the test set used as the estimate of prediction error

Main finding: with few irrelevant predictors, KNN is expected to do better
because it captures the non linear relationship. With many irrelevant
predictors, lasso is expected to do better because it shrinks the noise
coefficients to zero, while KNN suffers from the extra variance.

## Part B: Elastic net vs GAM (predicting depression severity)

Goal: predict depression severity 12 months after the start of a study from 20
baseline characteristics of adults with anxiety and/or depressive disorders
(1500 subjects).

Approach:
* Random split into training (1000) and test (500) data
* Elastic net (alpha = 0.5, lambda chosen with cross validation)
* Generalized additive model with smooth terms for continuous predictors
  (REML estimation)
* Comparison of test set MSE and R squared

Results reported in the original coursework: GAM had a slightly lower test MSE
(20.23) than the elastic net (20.69), with an R squared of about 0.30 for both.
Exact numbers may differ slightly with the seed used in this repository.

## Tools

R, caret, glmnet, mgcv, readr

## Data

The data files are not included, because they are not publicly shareable. The
code expects `Data.csv` and `MHpredict.csv` in the working directory, so file
paths may need to be adjusted.
