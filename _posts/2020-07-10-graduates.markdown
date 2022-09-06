---
layout: post
title:  "2020 Graduates! Xiaoyue Li, Dmitry Shemetov"
date:   2020-07-10 00:00:00 -0700
categories: students
---

Congrats to two Ph.D. graduates from my lab: Xiaoyue Li and Dmitry Shemetov!

### Xiaoyue Li

Xiaoyue's thesis is on scalable methods for point process data.  The dissertation consists of three main chapters.

1. Non-negative tensor decompositions for Poisson data
2. Changepoint estimation in multivariate Poisson processes
3. Deep learning for Cox proportional hazards models

I will devote another post to (1) when the relevant paper is published, but I'd like to highlight (2).  In 2 the data consists of time-stamped events.  In this problem, you want to determine the rates of each Poisson process, which each form a dimension in a vector (or a label).  You may believe for whatever reason that the intensities have dramatic systemic changes where all of the intensities for the different processes change at once.  The trick is to find these changepoints but do so with a computational complexity that scales with the number of events, not some artificial time discretization.

With the help of our collaborator Robert Bassett, Xiaoyue came up with two such methods.
1. A Frank-Wolfe algorithm for solving a group fused lasso optimization
2. A wild binary segmentation for multivariate Poisson processes

It turns out that these two can have very different behaviors, probably owing to the convex relaxation in the fused lasso.  You can see some resulting approximations below...

![](/images/changept_comp.png)

### Dmitry Shemetov

Dmitry's thesis is on detection in graphs, but this title does not do justice to the dramatically different problems that he tackles in his work.
1. Graph scan statistics with false discovery rate control
2. Compressed statistics in hierarchies
3. Graphlet sampling and exponential random graph models

(2) is a very theoretical work that gets at achievable signal-to-noise limits for performing a hypothesis test using hierarchical communication.  Basically the idea is that there is a hierarchy of computing nodes that receive a single bit from each child node and passes a single bit to the parent.  The idea is that at each step the nodes have to send a quantized version of the likelihood ratio test statistic.  The challenge is to quantify the loss of information due to this process.

(3) builds on [this work on efficient graphlet sampling](https://dl.acm.org/doi/pdf/10.1145/3292500.3330995) and shows that it can be used to estimate the parameters in an ERGM.  Finally, (1) uses graph scan statistics to localize outbreaks of porcine reproductive and respiratory syndrome (PRRS) in a network of pig farms.  Here is an illustration of the mobility network in the pig farms.

![](/images/pig_mobility.png)