---
id: w10-dehuili2-oob-selection-optimism
title: "Why can the lowest OOB error be optimistic after tuning?"
author: dehuili2
---

In Homework 10 Question 2, I compared 16 combinations of `mtry` and node size using OOB misclassification error. The default forest misclassified 14 of 327 training observations, while the selected setting misclassified 11. Each observation's OOB prediction uses only trees that excluded it from their bootstrap samples, so I initially thought the selected OOB error should also provide a fair assessment of the final model.

Why can choosing the smallest OOB error make that reported value optimistic, even though every candidate uses OOB predictions?

To isolate model selection from preprocessing, suppose the predictor representation is fixed independently of these observations. Consider several candidate settings with the same true generalization error but noisy, possibly correlated OOB estimates. Can a small numerical example explain why selecting the minimum favors favorable estimation noise, and why expanding the grid might lower the reported OOB error without improving prediction? How does reserving an independent test set address this problem?
