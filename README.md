# Naive-Bayesian-Classifiers
Bayesian inference to produce a simple multiclass classifier

In this tutorial, we will use our knowledge of Bayesian inference to produce a simple multiclass classifier. More specifically, if we have an input $\mathbf x$ (e.g. lab measurements of a patient), we aim to construct a model which can predict a corresponding label $y$ (e.g. a diagnosis). In our investigations, we will use vectorial data (i.e. $\mathbf x \in \mathbb{R}^D$) and integer labels (i.e. $y \in \left\lbrace 1, 2, \ldots, K\right\rbrace$). Our strategy will be as follows:

1. We take some samples $\mathbf x_i$ with known labels $y_i$ (training set) and use these to tune the model parameters (which is called training the model),
2. We use the trained model to produce predictions on new samples $\mathbf x$ (test set).

## A Bayesian take on classification

The posterior probability of an input $\mathbf x$ belonging to the $k$ th class can be written using Bayes' rule as
\begin{align*}
p\left(y=k \;\mid\; \mathbf x\right) = \frac{p\left(\mathbf x \;\mid\; y=k\right)p\left(y=k\right)}{p\left(\mathbf x\right)} .
\end{align*}
We aim to find the most probable class for the input. Since the denominator is the same for all $k$, we can safely ignore it:
\begin{align*}
p\left(y=k \;\mid\; \mathbf x\right) \propto p\left(\mathbf x \;\mid\; y=k\right) p\left(y=k\right).
\end{align*}

Now we have to estimate the quantities on the right using the training set.
- $p\left(y=k\right)$ is easy as we can just use the ratio of samples belonging to class $k$ in the training set.
- $ p\left(\mathbf x \;\mid\; y=k\right)$ is somewhat more involved. Let as assume that the entries in a sample $\mathbf x$ are independent (a very naive assumption) and follow a Gaussian distribution. Formally, we assume that
\begin{align*}
p\left(\mathbf x \;\mid\; y=k\right) &= p\left(\mathbf x^1 \;\mid\; y=k\right) \cdot p\left(\mathbf x^2 \;\mid\; y=k\right) \cdots p\left(\mathbf x^D \;\mid\; y=k\right),\\
p\left(\mathbf x^l \;\mid\; y=k\right) &= \mathcal N \left(\mathbf x^l \;\mid\; \mu_k^l, {\sigma^2}_k^l \right),
\end{align*}
where $\mathbf x^l$ denotes the $l$ th component of $\mathbf x$. Now the only thing keeping us from making predictions is that we don't know $\mu_k^l$ and ${\sigma^2}_k^l$. However, they are easily estimated using the mean and variance of the $l$th component of the samples belonging to class $k$ in the training set.

This model is called Naive Bayes and despite its simplicity, it tends to perform fairly well on a large number of problems.
