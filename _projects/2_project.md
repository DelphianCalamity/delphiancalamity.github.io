---
layout: page
title: DeepReduce
# description: a project that redirects to another website
img: assets/img/conflict-sets.png
# redirect: https://unsplash.com
importance: 5
category: Research
github: https://github.com/DelphianCalamity/horovod.git

---

I developed a compressed communication mechanism for distributed machine learning using bloom filters. When training neural networks in a distributed setting with data parallelism each replica of the model generates its own local gradients. Those gradients need to be broadcasted and aggregated so that they are used for the update of the replicas. This creates a significant communication bottleneck that gets mitigated through the compression of the gradients. I developed two TensorFlow operators for encoding and decoding the indices of sparsified gradients, as those were produced during the training of deep neural networks. The encoded output was a bloom-filter which is lossy in nature, so the inaccurate reconstruction of the gradients was degrading the accuracy of the models. To remedy that, I developed the “false-positive-aware” mechanism, a compression method that adaptively modifies the encoded gradient based on its knowledge for all the future bloom-filter errors.
