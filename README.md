#Paper Recreation

Implementation of paper:  [Learning from Randomly Initialized Neural Network Features](https://arxiv.org/pdf/2202.06438)

[see also](https://www.coreauto.com/blog/how-our-data-shaped-neural-architecture-discovery-and-how-automation-can-reshape-the-future)

The implementation has some adjustments. Since I didn't have the budget to run the model a GPU outside of Colab, I reduced the number of samples we take (eg the number of models
generated) and upped the dimension of each model output. This likely introduces more noise, since the estimates will have converged less for each example. Parallelization could help
with this, and is the next step.
