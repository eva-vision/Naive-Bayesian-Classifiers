# Naive-Bayesian-Classifiers
Bayesian inference to produce a simple multiclass classifier

In this tutorial, we will use our knowledge of Bayesian inference to produce a simple multiclass classifier. More specifically, if we have an input $\mathbf x$ (e.g. lab measurements of a patient), we aim to construct a model which can predict a corresponding label $y$ (e.g. a diagnosis). In our investigations, we will use vectorial data (i.e. $\mathbf x \in \mathbb{R}^D$) and integer labels (i.e. $y \in \left\lbrace 1, 2, \ldots, K\right\rbrace$). Our strategy will be as follows:

1. We take some samples $\mathbf x_i$ with known labels $y_i$ (training set) and use these to tune the model parameters (which is called training the model),
2. We use the trained model to produce predictions on new samples $\mathbf x$ (test set).

