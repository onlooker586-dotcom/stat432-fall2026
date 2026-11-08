---
id: w11-dehuili2-kmeans-point-relocation
title: "How can moving one point improve a converged K-means solution?"
author: dehuili2
---

In Homework 11 Question 1, two random starts converged to different groupings, with within-cluster sums of squares (WCSS) of 4.468452 and 4.566039. After accounting for arbitrary cluster labels, only observation 10 changed groups. Moving that observation in the worse solution and recomputing both cluster means produces the better solution. Yet the worse solution had already stopped changing under the usual K-means updates.

How can relocating a point reduce WCSS when that point is already assigned to its nearest current mean?

Suppose a point $x$ moves from cluster $A$ to cluster $B$, with current sizes $n_A>1$ and $n_B\geq1$ and means $m_A$ and $m_B$. Assuming all other assignments stay fixed, can we derive the exact change in WCSS after recomputing both means? How does this criterion differ from comparing $\lVert x-m_A\rVert^2$ and $\lVert x-m_B\rVert^2$ with the means held fixed, and why unchanged Lloyd assignments do not rule out an improving move?
