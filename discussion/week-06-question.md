---
id: w06-dehuili2-knn-training-auc
title: "Why k = 1 KNN Achieves a Perfect Training AUC"
author: dehuili2
---

In Question 2 of Homework 6, KNN with k = 1 achieves a training AUC of exactly 1.0000 but a test AUC of only 0.8962. Why must the training AUC equal 1 at k = 1? For each training observation, the distance to itself is 0, so its nearest neighbor is itself and the fitted probability equals its own label (0 or 1); every training point is thus ranked perfectly.

Is this always guaranteed? Suppose two training observations have identical features but different labels, and ties are broken by the smaller row number. The later observation's nearest neighbor becomes the earlier one, so its fitted probability equals the other observation's label, not its own. Can the training AUC still be exactly 1 in this case?

What does this reveal about why training performance, especially at small k, does not reflect performance on new observations?
