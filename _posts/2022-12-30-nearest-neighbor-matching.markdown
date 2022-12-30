---
layout: post
title: 'Nearest neighbor matching deserves a second look'
date: '2022-12-30'
categories: research
---

## New results on consistency of nearest neighbor matching

I published (finally) my paper on Nearest Neighbor Matching (NNM) in IEEE TransIT.
It basically shows that if you have a biased non-missing sample and a unbiased partially missing sample, where X is non-missing and Y is missing for the population of interest, then it works to just match the partially missing data to the non-missing biased sample to estimate the population mean of Y.
This is NNM, and we know that it is consistent when the two distributions satisfy a Renyi entropy constraint and the expectation of Y given X satisfies a moment constraint.
Previously, it was known that it was consistent under Lipschitz smoothness constraints (which is easy to show) and we even had rates!  Unfortunately, these rates were suboptimal under the Lipschitz assumption.
So, debiasing approaches were proposed, but at that point it was unclear why you would not just use model based or regression approaches.
However, without the Lipschitz assumption it is much harder to show even consistency.
This is what I established, but there are many questions that I have!

## Open problems for NNM

1. Minimax optimal?
2. Rates?
3. 
