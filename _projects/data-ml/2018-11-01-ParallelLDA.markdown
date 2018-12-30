---
title: ParallelLDA
description: Implementing Parallel LDA for Text Classification using OpenMPI
note: Through implementing parallel LDA and experimenting with its performances, I gained a deeper understanding of the use of parallel systems in text mining and NLP use cases.
date: 2018-11-01 19:55:16
---

\#MachingLearning \#TextClassification \#ParallelSystems \#LDA

This is a final project for CMU 15-418: Parallel Computer Architecture and Programming.

### Introduction

Latent Dirichlet Allocation (LDA) is a widely used algorithm in text classification, which clusters word occurrences into latent classes (i.e. topics) after iterations of parameter learning. As the sampling process is extremely computation-heavy for large data sets, we implemented parallel LDA in this project and experimented with its performance.

### LDA at a Glance

![Image]({{ site.baseurl }}/images/projects/lda-intro.jpg)

### Method

Parallel LDA workflow: 
* Split corpus by document
* Each process runs local Gibbs sampling
* Master gathers updates and send back to each process

![Image]({{ site.baseurl }}/images/projects/lda-workflow.jpg)

### Implementation

We implemented two variations of parallelism LDA using the OpenMPI library - the synchronous version and the asynchronous version. We also added staleness in our implementation.

* Synchronous Parallel LDA: updates broadcasted to all processes
* Asynchronous Parallel LDA: each process send local updates to master after a few iters, keep on sampling, and updates upon receiving new table

### Results

![Image]({{ site.baseurl }}/images/projects/lda-result.jpg)

### Discussion

* How does the parallelism scale? 
Close to linear speedup until ~6 procs, and gets smaller after but still achieves 9x with 16 procs.
* What's the tradeoff between log-likelihood & speed?
Learned parameters will be more “stale” as the staleness gets larger. This gets us faster speed, but sometimes might decrease the objective function (log-likelihood) as a tradeoff.
* Speedup comparison of sync vs. async
We expected async version to be faster, but since there’s not much work imbalance in sync version, and for async the master takes on more work updating the tables based on messages from each process, the speedup for both are about the same.

### Conclusion

Our implementation of parallel Latent Dirichlet Allocation achieves an overall good speedup compared to the sequential version. For future work, better asynchronous update rules might be designed for better work balance to further improve performance.

### Code

[ParallelLDA](https://github.com/judykong97/Parallel_LDA)

### Team Members

[Zhixin(Angelica) Feng](https://www.linkedin.com/in/zhixin-angelica-feng)

