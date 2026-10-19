---
id: w08-dehuili2-slack-versus-errors
title: "Why can a larger SVM cost fail to reduce training mistakes?"
author: dehuili2
---

Why does increasing $C$ in a soft-margin SVM penalize margin violations more strongly without necessarily reducing the number of training classification errors?

My intuition is that making margin violations more expensive should encourage the classifier to correct more mistakes. However, the objective penalizes the total magnitude of margin violations, whereas the classification error count only measures how many observations are misclassified. Correctly classified observations inside the margin also contribute positive slack.

For a fixed training dataset and predictor scaling, suppose we fit models using a smaller and a larger value of $C$ and obtain a global optimum in each case. Can we use their optimality conditions to prove that total slack cannot increase as $C$ increases? Then, can a small example illustrate how the number of training classification errors could increase even when total slack decreases?

Assume that no fitted score is exactly zero, to avoid classification ties.
