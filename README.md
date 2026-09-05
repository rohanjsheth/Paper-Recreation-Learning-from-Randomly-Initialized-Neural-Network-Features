# Paper Recreation

An adaptation of [Learning from Randomly Initialized Neural Network Features](https://arxiv.org/pdf/2202.06438).

See also: [the authors’ accompanying blog post](https://www.coreauto.com/blog/how-our-data-shaped-neural-architecture-discovery-and-how-automation-can-reshape-the-future).

To work within my Colab compute budget, I use fewer independently initialized ResNet-18 models and concatenate the 512 pooled features from each. The paper instead extracts one scalar output per independent network initialization.

This reduces the number of forward passes, but changes the sampling procedure. Features from the same network can be correlated, so increasing each model’s output dimension does not provide the same diversity as sampling more independent networks.

The next step is to benchmark parallel feature extraction, with the goal of improving throughput and running more independent initializations.
