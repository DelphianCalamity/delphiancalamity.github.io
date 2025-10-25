---
layout: page
title: Sangria
# description: a project that redirects to another website
img: assets/img/heat.png
# redirect: https://unsplash.com
importance: 3
category: Research
github: https://github.com/columbia/sangria

---

Strict Two-Phase Locking (2PL) combined with Two-Phase Commit (2PC) remains the standard approach for ensuring strict serializability and atomicity in distributed transactions. However, its conservative strategy of holding locks throughout the full duration of the commit process amplifies the contention footprint of transactions, limiting throughput and latency under high-contention workloads. Relaxed variants, such as Early Lock Release (ELR), improve concurrency through pipelining: by releasing locks earlier in the commit protocol, subsequent transactions can acquire locks and proceed before prior commits complete. However, this introduces commit-time dependencies that require additional coordination and risk cascading aborts. No single protocol excels across all workload conditions and resource availability, yet most distributed systems hardcode one fixed strategy — designed for specific assumptions while sacrificing generality.
This paper introduces Sangria, a novel distributed commit protocol that dynamically adapts its commit strategy to exploit the complementary strengths of both conservative and relaxed approaches. Unlike traditional designs that enforce a single, fixed commit strategy across the entire system, Sangria provides fine-grained adaptability: each participant involved in the transaction — typically corresponding to an accessed data item — independently adjusts its commit behavior based on its local contention and general resource availability. By intelligently balancing between conservative and relaxed commit modes at runtime, Sangria dynamically optimizes performance under varying conditions while preserving the strong consistency guarantees inherent to each mode. This work opens the door to a more flexible, workload-aware approach to distributed transaction management — where transactions no longer commit rigidly, but instead dance to the rhythm of the workload.
 <br>

