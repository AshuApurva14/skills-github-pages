---
title: "Kubernetes Troubleshooting: A Step-by-Step Guide"
date: 2026-03-09
---
Microservice architecture and Kubernetes have become a globally adopted solution in software development for the organization looking for `Scalability` and `Operational Efficiency`. 

The following errors will be discussed:

- Container CRASHBACKLOOP (OOM Killed and CPU Throttling)
- ENV variables/secret mount
- DB Connectivity 

---

**Container CRASHBACKLOOP issue**

<img width="1000" height="500" alt="Image" src="https://github.com/user-attachments/assets/625d39a0-90a9-4297-b626-eb2ea2e64f52" />

1. The CRASHBACKLOOP issue is generally encountered when the container crashes due to an  internal code failure or is unable to connect to its required dependencies. 
2. The Kubelet is responsible for creating the pods and starting the containers inside them. As containers keep crashing, the kubelet tries to restart, leading to a crash loop.
3. In this crash loop, there is a time delay between containers crashing and containers restarting; that is the backoff time, which keeps increasing with each restart.

