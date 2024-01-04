---
layout: page
title: TF DTensor LM training with collective optimization on GPU
description: Research project at Google - A performance study on BERT and T5 training using TF DTensor on GPU.
img: assets/img/gpu_cover_img.jpeg
importance: 2
category: research
giscus_comments: true
---

[DTensor](https://www.tensorflow.org/guide/dtensor_overview) is a distributed computing API for Tensorflow. My internship project at Google for summer 2023 is to design, explore and develope an optimization method for DTensor all-reduce collectives on GPU with [Nvidia NCCL](https://developer.nvidia.com/nccl) enabled.

The new optimization for DTensor is now available to use via specifying the environment variable: `DTENSOR_ALL_REDUCE_COMBINER_TOPOLOGICAL_DISTANCE_OPTIMIZATION`.

With the introduction of the new optimization, a performance study is conducted on model training for BERT and T5. 160 train steps are profiled for each sets of configurations, and total of 48 training experiments are ran with 8 GPUs on P100.

Detail experiment report / publically content under review.
