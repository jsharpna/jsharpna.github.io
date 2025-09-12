---
layout: post
title: "NeurIPS 2024 Workshop Keynote: Building a High Stakes Online Test with Human-in-the-loop AI"
date: 2024-12-16 00:00:00 -0700
categories: events
---

I had the honor of delivering a keynote talk at the NeurIPS 2024 Workshop on Large Foundation Models for Educational Assessment. The talk focused on "Building a High Stakes Online Test with Human-in-the-loop AI," presenting our comprehensive approach to constructing the Duolingo English Test (DET).

## Abstract

In this talk, we present a comprehensive overview of the construction of the Duolingo English Test (DET), a high-stakes, large-scale, fully online English language proficiency test built using human-in-the-loop (HIL) AI. The DET is a computerized adaptive test where test takers respond to items designed to assess their proficiency in speaking, writing, reading, and listening. Human oversight plays a critical role in ensuring the DET's fairness, lack of bias, construct validity, and security. Additionally, AI and foundation models enable the scalability of key processes, including real-time security features and automated scoring.

We will take a tour of this process, organized into five parts. First, items are constructed using generative AI models like GPT, followed by human review to evaluate potential bias and fairness. Second, machine learning models automatically grade items by predicting expert human ratings based on construct-aligned AI features. Third, items are calibrated using explanatory item response theory models and custom item embeddings, aligning them with historical test taker performance. Fourth, tests are administered via Thompson sampling, motivated by framing computerized adaptive testing as a contextual bandit problem, and scored using a fully Bayesian approach. Finally, automated AI signals, such as eye-gaze tracking and LLM response detection, support proctors in detecting cheating and ensuring adherence to test rules. Throughout this process, humans and AI collaborate seamlessly to maintain the DET's integrity and effectiveness.

## The Five-Part Framework

The talk covered our systematic approach to building a reliable, scalable, and fair language assessment:

1. **Item Construction**: Leveraging generative AI models like GPT for initial item creation, followed by rigorous human review for bias and fairness evaluation.

2. **Automated Scoring**: Employing machine learning models that predict expert human ratings using construct-aligned AI features.

3. **Item Calibration**: Implementing explanatory item response theory models with custom item embeddings to align with historical performance data.

4. **Adaptive Testing**: Using Thompson sampling within a contextual bandit framework for test administration, combined with fully Bayesian scoring approaches.

5. **Security and Integrity**: Deploying automated AI signals including eye-gaze tracking and LLM response detection to support human proctors in maintaining test security.

You can view the full keynote details at [NeurIPS 2024](https://neurips.cc/virtual/2024/107597).
