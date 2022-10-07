---
layout: page
title: DeepReduce: A Sparse-tensor Communication Framework for Federated Deep Learning
# description: a project with a background image
img: assets/img/3.jpg
importance: 2
category: work
---

I developed a compressed communication mechanism for distributed machine learning using bloom filters. When training neural networks in a distributed setting with data parallelism each replica of the model generates its own local gradients. Those gradients need to be broadcasted and aggregated so that they are used for the update of the replicas. This creates a significant communication bottleneck that gets mitigated through the compression of the gradients. I developed two TensorFlow operators for encoding and decoding the indices of sparsified gradients, as those were produced during the training of deep neural networks. The encoded output was a bloom-filter which is lossy in nature, so the inaccurate reconstruction of the gradients was degrading the accuracy of the models. To remedy that, I developed the “false-positive-aware” mechanism, a compression method that adaptively modifies the encoded gradient based on its knowledge for all the future bloom-filter errors.
