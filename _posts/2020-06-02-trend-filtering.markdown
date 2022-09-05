---
layout: post
title: 'Trend Filtering: what we know and the future'
date: '2020-06-02 00:00:00 -0700'
categories: theory
---

## Trend filtering

Trend filtering is an estimator that uses discrete differences to smooth a noisy vector (or more generally, tensor).
The method was proposed and computational methods were studied in the 2000's for data on multidimensional grids.
Basically, it takes the general form,

$$\sum_i \ell(\beta_i; y_i) + \lambda \| D^{(k)} \beta \|_1$$

where D is a discrete differencing operator.  The k is the order, basically, for k of 1 you get piecewise constant signal, and for higher k you get piecewise polynomials.
FYI trend filtering with k of 1 is called the fused lasso or total variation denoising (for one of my papers I regrettably tried to rename this the 'edge lasso' when applied to graphs).
The nice thing about this is that you get automated knot selection, which happens because you are using an L1 penalty.
This gives you *local adaptivity*, which is when your estimator adapts to the local smoothness of the underlying signal.
You can use this with most losses, for example, the Poisson loss can give you locally adaptive histograms,

![Fused histogram](/images/fused_hist.png)

## Graph trend filtering

It is pretty straightforward to define the fused lasso (k=1) over graphs, you just let D be the incidence matrix, which turns the penalty into the L1 of the difference across edges of the graph.
For higher order graphs, we had to make some choices, and what we settled on is

$$ D^{(k+1)} = \Big\{ \begin{array}{ll} D^\top D^{(k)},& k~{\rm odd} \\ D D^{(k)}, & k~{\rm even} \end{array}. $$

This has the desired local adaptivity property, as evidenced by this example over the Allegheny county zip codes (it varies the smoothness locally) which are connected based on direct proximity:

<p align='center'>
<img src='/images/GTF_allegheny.png'>
</p>

## What we know

So after years of studying trend filtering we have some things that we do know (about theory).
First, I would like to call out two types of results,

1. L0 rates: these are results that assume that true signal satisfies a sparsity assumption, that there are only s non-zero discrete derivatives.  Typically, the hope is to recover the standard 'parametric' rates of the lasso, $$ \| \hat \beta - \beta_0 \|^2 \lesssim s~{\rm plog} n$$ for some choice of tuning parameter and $$\beta_0$$ is the true signal.

2. L1 rates: these are results that assume that the true signal have only bounded L1 norm (total variation), i.e. $$\| D \beta \|_1$$ is bounded.  Typically, here you show that $$ \| \hat \beta - \beta_0 \|^2 \lesssim n^\alpha~{\rm plog} n$$ for some choice of tuning parameter.


The problem with 1, is that you can get the parametric rates regardless of the graph structure (as long as it is connected) for the fused lasso.  We showed this with the depth-first-search (DFS) wavelets (at least for the fused lasso) in [this paper](https://www.jmlr.org/papers/volume18/16-532/16-532.pdf).
Basically, 1 only requires a tree structure and not a more highly connected graph structure.
It is substantially harder to show this for higher order trend filtering, even in 1 dimension (see [this paper](https://arxiv.org/abs/1702.05113) by Guntuboyina et al. and [our prior work](https://proceedings.neurips.cc/paper/2017/file/5abdf8b8520b71f3a528c7547ee92428-Paper.pdf)), and there is a loss in log factors if you go with the DFS wavelet approach.
The satisfying thing about results of type 2 is that the rate parameter $$\alpha$$ depends on the graph structure, and smaller typically means a more connected graph.
For this reason, I have focused on this type of result.

There *is* a third type of result, which gives you exact reconstruction of the region where you have polynomial structure.  I attempted this in [this paper](https://proceedings.mlr.press/v22/sharpnack12.html), but the conditions are ridiculous.  I believe that this is insurmountable, and I provide some evidence.

So, what do we know?
1. Rates for Gaussian noise, grid graphs ([Veeru Sadhanala's](https://www.cs.cmu.edu/~vsadhana/) thesis, [this paper](https://proceedings.neurips.cc/paper/2017/file/3e60e09c222f206c725385f53d7e567c-Paper.pdf))
2. [Rates for density estimation](https://arxiv.org/abs/1805.03288), in 1 dimension (and 'geometric graphs') with k=1 (fused lasso).
3. [A base rate for all connected graphs](https://www.jmlr.org/papers/volume18/16-532/16-532.pdf) with k=1, spoiler, it is the same as the 1D fused lasso $$n^{1/3}$$.
4. [A tool, called eigenvector incoherence](https://arxiv.org/abs/1410.7690), for analyzing any order over any graph that is tight in some cases.
5. [A specialized result](https://academic.oup.com/biomet/article/107/2/293/5717457) for k=1, nearest neighbor graphs, turns out that the rate is the same for grids on the intrinsic dimension of the manifold.
6. [Rates for additive trend filtering models](https://arxiv.org/abs/1702.05037)
7. [Lower bounds for multidimensional trend filtering](https://arxiv.org/abs/2112.14758)

## Future work (that I probably will not pursue myself)

So there is a lot that we don't know, here are some thoughts.

1. The eigenvector incoherence tool gives us a method for analyzing any graph, but it is very opaque.  It would be better if we could relate the rates to a functional of the graph that is more interpretable and easier to analyze.
2. General exponential families are mostly wide open.
3. Rates for trend filtering in high dimensions under strong sparsity assumptions.
4. There are strange behaviors for higher order GTF on point clouds in multiple dimensions, particularly at the boundaries of the support.  For $$k=1$$ this goes away, but at higher order, we need to modify GTF.  Our best guess at the ideal approach is to come up with a fine spline basis and then come up with the trend filtering penalty on this.