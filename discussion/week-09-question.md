---
id: w09-dehuili2-small-gamma-linear-limit
title: "Does a small RBF gamma really make an SVM linear?"
author: dehuili2
---

In Homework 9 Question 1, RBF with $C=1$ and $\gamma=0.01$ achieved mean CV error 0.2684, close to 0.2728 for linear SVM with $C=0.1$. The lecture explains that smaller $\gamma$ makes similarity decay more slowly. Does making $\gamma$ very small turn an RBF SVM into a linear SVM, or can it simply make the classifier too strongly regularized?

For standardized predictors, the radial kernel is

$$
K(\mathbf{x},\mathbf{z})=\exp(-\gamma\|\mathbf{x}-\mathbf{z}\|^2).
$$

As $\gamma$ approaches zero, all kernel values approach one, which seems different from the linear kernel $\mathbf{x}^{\mathsf T}\mathbf{z}$.

Using a first-order expansion of the radial kernel and the dual constraint $\sum_i\alpha_i y_i=0$, can we explain when a small-$\gamma$ RBF SVM behaves approximately like a linear SVM and how its effective regularization depends on both $C$ and $\gamma$? In particular, how should $C$ change as $\gamma$ decreases to preserve a comparable fit, and why does this motivate tuning them jointly?
