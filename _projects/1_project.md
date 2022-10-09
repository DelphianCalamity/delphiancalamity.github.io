---
layout: page
title: DPack
# description: a project with a background image
# img: assets/img/12.jpg
importance: 1
category: Research
github: https://github.com/DelphianCalamity/PrivateKube.git
---

DPack is a framework that aims to maximize the exploitation of private datasets when using differential privacy. Differential privacy theoretically bounds the privacy loss when querying a dataset. Every time a data scientist analyzes a dataset through the execution of queries they “consume” privacy budget. Since privacy loss is bounded there is only a finite number of queries that a dataset can answer before breaking the privacy guarantees. In this work, we view the privacy that will be consumed by the queries  as a new scheduling resource, which is a first-class citizen alongside other traditional computing resources, such as CPU, memory and network bandwidth. The goal of DPack is to execute queries in a schedule that maximizes the total number of queries that can be processed or the total utility that can be achieved given also the importance of each query. 
In this work, we reduce this scheduling problem to an optimization problem and implement a tool that simulates the dynamic arrival of data and queries and a scheduler that is responsible for allocating privacy resources for the execution of the queries. Finally, we incorporated the scheduler to a real, open-sourced resource orchestrator to enable its broader applicability. We chose to integrate DPack with Kubernetes, the most popular resource orchestrator in cloud systems. I took part in all aspects of this project, and was solely responsible for the systems side: the design and implementation of DPack in Kubernetes.