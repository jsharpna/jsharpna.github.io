---
layout: post
title: 'Nearest neighbor matching deserves a second look'
date: '2022-12-30'
categories: research
---

## New results on consistency of nearest neighbor matching

I published (finally) my paper on Nearest Neighbor Matching (NNM) in IEEE TransIT.
It basically shows that if you have a biased non-missing sample and an unbiased partially missing sample, where X is non-missing and Y is missing for the population of interest, then it works to just match the partially missing data to the closest non-missing biased sample to estimate the population mean of Y.
This is NNM, and we know that it is consistent when the two distributions satisfy a Renyi entropy constraint and the expectation of Y given X satisfies a moment constraint.
Previously, it was known that it was consistent under Lipschitz smoothness constraints (which is easy to show) and we even had rates!  Unfortunately, these rates were suboptimal under the Lipschitz assumption.
So, debiasing approaches were proposed, but at that point it was unclear why you would not just use model based or regression approaches.
However, without the Lipschitz assumption it is much harder to show even consistency.
This is what I established, but there are many questions that I have!

One nice thing is that it works for any Borel measurable regression function, but a downside is that it requires finite dimensions and a density.
In fact, we are awfully close to showing that this can work without the finite dimensionality assumption.
I outlined in that paper how we can prove this for a broader set of separable metric spaces.
But it requires some new results which would typically be lemmas for nearest neighbor regression.
Then the remainder of my results would extend pretty naturally to this setting.

Nearest neighbor matching is very appealing because it can be used in combination with any metric and can benefit from data structures that target nearest neighbor lookups.
For example, you could imagine a situation where an SQL query in a massive distributed data set, i.e. search applications, is

```
select average(Y) from bigtable where X < 1
```

If Y was partially missing then you could just match the missing entries to the non-missing entries and then use NNM.
This situation is pretty common in search, especially for logs.
Any search engine with an HNSW backend can do this on the fly.

## Open problems for NNM

1. Minimax optimal? We know that NNM is not optimal under smoothness assumptions, but we aren't sure about general Borel measurable regression functions.  It may be that in this more general setting estimating moments from biased samples is just really hard.
2. Rates?  Do we have nontrivial rates? It's not even clear if we should expect any.
3. Combining this with metric learning.  One natural way to create a deep learning variant of this is to use metric learning for the supervised task of estimating Y given X over the biased sample.
