---
layout: page
title: Recursion in TensorFlow
# description: a project that redirects to another website
img: assets/img/tree.jpeg
# redirect: https://unsplash.com
importance: 3
category: Research
github: https://github.com/DelphianCalamity/tensorflow-recursion.git
---

I investigated how recursive functions can be supported in dataflow systems and especially TensorFlow. The challenge was to create dataflow graphs that can capture the logic of recursive functions without being dynamically expanded at runtime. Static dataflow graphs enable a variety of graph optimizations that can accelerate the training of recursive neural networks, which are widely used in natural language processing.
I enabled the support of recursion in TensorFlow through extending its API, enforcing graph transformations that make the graphs static during their execution and extending its execution engine with a tagging mechanism that enables the correct execution of those graphs.
