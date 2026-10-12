---
id: w07-dehuili2-bias-variance-trade-off
title: "Why is LDA's test error flat in rho while QDA's drops sharply?"
author: dehuili2
---

In the Question 3 simulation output: LDA's average test error stayed almost constant near 0.17 for every $\rho$, while QDA dropped from about 0.20 ($\rho=0$) to 0.10 ($\rho=0.9$). Why is LDA so insensitive to the covariance structure, and when does the shared-covariance assumption actually become costly?

My guess is that the pooled covariance, being an average of the two class covariance matrices, somehow cancels the $\rho$ dependence, but I am not sure whether that is right or why it would happen. And from the bias-variance view: QDA pays a variance cost at small $\rho$ and buys bias reduction at large $\rho$ — where do the eight noise covariates shift that trade-off?