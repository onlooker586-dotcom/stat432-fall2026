---
id: w05-dehuili2-distance-measures
title: "Which distance measure fits which data type?"
author: dehuili2
---

In lecture we used Euclidean distance for KNN, but different data express similarity differently. How should we choose between Euclidean distance, Manhattan distance, and cosine similarity when features are pixel, word counts, or mixed continuous and categorical variables? Is there a principled criterion, or is it trial and error?

A concrete example shows the difference. For the origin and points (1,0), (0,1), and (0.6,0.6), Euclidean distance makes (0.6,0.6) the nearest neighbor, while Manhattan distance makes (1,0) and (0,1) equally close, so the chosen measure changes both the neighbor and the tie rule.

This matters in our Homework 5 setting: with 30 covariates, many strongly correlated, Euclidean distance treats repeated information as new information and lets correlated variables dominate the neighborhood. Would Manhattan distance behave differently? Does this mean the choice of distance is as important as the choice of k?
