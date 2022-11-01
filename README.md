# Study project. 

# Data Science course at Tomsk State University

Goal: forecast bank client churn.

Original dataset (not published; school property): 355190 rows, 234 columns.

Class 0: 92%; class 1: 8%.

Data preparation:

- Scaling of continuous variables

- Removal of missing values

- One hot encoding of categorical variables

- There are almost 10 thousand different job positions but most are represented by only a few people. Only the most common positions were selected.

Metrics selected deal with class imbalance and greater importance of the smaller class.

Various methods and ensembles tested.

Random forest did not improve results compared with a single tree, likely because variance is small due to the large sample size so the problem normally solved by random forest was not there in the first place. Gradient boosting performed worse than a single tree.

Results (recall, ROC AUC) were improved by a combination of a decision tree with Ada Boost.

Files:

data_prep.ipynb – data preparation

predict_churn.ipynb – model selection and training

predict_churn_neural.ipynb – solution with a neural network.

