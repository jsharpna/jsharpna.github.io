---
layout: post
title:  "Liwei Wu defends thesis: Advances in Collaborative Filtering and Ranking"
date:   2020-02-20 00:00:00 -0700
categories: group
---

[Liwei Wu](http://anson.ucdavis.edu/~liweiwu/index.html) (advised by myself and Cho-Jui Hsieh) recently defended his outstanding thesis in my department.  In his research, Liwei has continually pushed the frontier of recommendation system research by identifying important outstanding problems in this domain, solving them, and communicating his findings in top machine learning conferences.  His work has been published in KDD, NeurIPS, ICML, CVPR, and AIStats, and four of these papers are the basis for chapters of his thesis.

Here he is presenting our work at NeurIPS 2019!
![NeurIPS](/images/liwei_neurips.jpg)

The first chapter (Ch 2) develops a method by which a knowledge graph can be incorporated into large-scale pointwise collaborative filtering.  This problem is important because quite often structural information for users and items in collaborative filtering comes in the form of a graph.  Many approaches such as using graph convolutional networks, are difficult to apply to large collaborative filtering datasets because the neighborhood size (the receptive field in GCNs) scales exponentially with depth.  This chapter proposes using the Bloom filter to encode deep graph information and it provides provable guarantees for the resulting method.  This paper will appear in AIStats 2020.

Earlier in Liwei’s research career, Liwei developed tools for training factorization based recommendation systems with novel ranking losses.  These appear in Chapters 3 and 4, which is on collaborative ranking in which users in a recommendation system have ranked or rated items and we would like to either recommend new items or denoise the empirical rankings by using all of the ratings together.  His first work on this topic, “Large-scale Collaborative Ranking in Near-Linear Time”, is the subject of Chapter 3 and was published in KDD 2017.  The topic is on using pairwise comparisons to learn latent user, item features that explain the observed ranking.  This work develops efficient algorithms that allow these methods to scale to massive datasets.

Liwei turned his attention to listwise ranking algorithms, the subject of Chapter 4, where a permutation based model is assumed as the generative process for a user’s ranking.  Liwei developed a fast implementation of the method, and performed exhaustive empirical comparisons with state-of-the-art methods.  Liwei showed that using the full list in the listwise model outperformed other simplified ranking losses.  This work has appeared in ICML.

Chapters 5 and 6 are on using deep learning methods with user embeddings.  Previous work had shown that incorporating user embeddings into attention models does not improve performance.  Liwei suspected that because user embeddings dramatically increase the number of parameters then this model tends to overfit and thus some form of regularization is required.  He developed a novel form of regularization called stochastically shared embeddings, which enabled personalized deep learning models to outperform their un-personalized counterparts.  Liwei followed this work with a more extensive analysis of a personalized transformer model for sequential recommendation (In submission).  This constitutes the current state of the art in recommendation systems as it incorporates ranking and temporal information in a collaborative fashion.
