# Naive-Bayesian-Classifiers
Bayesian inference to produce a simple multiclass classifier

In this tutorial, we will use our knowledge of Bayesian inference to produce a simple multiclass classifier. More specifically, if we have an input $\mathbf x$ (e.g. lab measurements of a patient), we aim to construct a model which can predict a corresponding label $y$ (e.g. a diagnosis). In our investigations, we will use vectorial data (i.e. $\mathbf x \in \mathbb{R}^D$) and integer labels (i.e. $y \in \left\lbrace 1, 2, \ldots, K\right\rbrace$). Our strategy will be as follows:

1. We take some samples $\mathbf x_i$ with known labels $y_i$ (training set) and use these to tune the model parameters (which is called training the model),
2. We use the trained model to produce predictions on new samples $\mathbf x$ (test set).

![image](https://github.com/eva-vision/Naive-Bayesian-Classifiers/assets/52841811/b4c73ef7-e9cd-48ac-9ea1-6b11298fe780)


![image](https://github.com/eva-vision/Naive-Bayesian-Classifiers/assets/52841811/c62e2268-eb90-4e65-9a14-2342721e1b76)


![image](https://github.com/eva-vision/Naive-Bayesian-Classifiers/assets/52841811/352c8159-1b06-41e9-ae7e-d373d40bd69c)


![image](https://github.com/eva-vision/Naive-Bayesian-Classifiers/assets/52841811/a6fdb7f6-bd8f-4372-8a70-ddf868987928)
