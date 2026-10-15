# R Projects: Supervised and Unsupervised Learning

This repository contains R code from two statistics and data science projects.
All analysis is in one R Markdown file:
`depression_prediction_and_personality_clustering.Rmd`

## Part A: Predicting depression severity (supervised learning)

Goal: predict depression severity 12 months after the start of a study, using 20
baseline characteristics of adults with anxiety and/or depressive disorders
(1500 subjects).

Approach:
* Random split into training (1000) and test (500) data
* Random forest, with mtry chosen by 5-fold cross-validation and the number of
  trees checked with the out-of-bag error
* Variable importance (%IncMSE and IncNodePurity) and partial dependence plots
* Test set accuracy measured with MSE and R-squared
* Prediction and uncertainty interval for a single new patient, using the
  predictions of the individual trees

Results reported in the original coursework: the random forest had the lowest
test MSE (20.05), compared with a GAM (20.22) and an elastic net (20.69). The
most important predictors were the IDS score, age at onset and LCImax. The
GAM and elastic net models were fitted in an earlier assignment, so their code
is not included here. This repository uses a different random seed, so exact
numbers may vary slightly.

## Part B: Personality data, PCA and clustering (unsupervised learning)

Goal: reduce 30 highly correlated personality variables to a small number of
components and use them to find groups of participants.

Approach:
* Number of components chosen with Kaiser's rule, scree plot, Horn's parallel
  analysis and Velicer's MAP test (all but the scree plot pointed to 5)
* Interpretation of the components using their loadings
* K-means clustering on the 5 components, with the number of clusters chosen
  from the proportion of variance explained and the sum of squared errors
* Hierarchical clustering (complete, average and single linkage) as a
  comparison
* Description of the clusters using their average component scores

## Tools

R, caret, randomForest, nFactors, EFA.dimensions

## Data

The data files are not included, because they are not publicly shareable. The
code expects the files `MHpredict.csv`, `Patient.csv` and `data.US.csv` to be in
the working directory.
