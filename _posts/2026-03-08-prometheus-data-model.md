---
title: Prometheus Data Model (Time Series + Labels)
date: 2026-03-08
---

Prometheus stores data as a time series.

A Time Series = **metric name** + **Labels** + **Timestamps** + **Value**

<img width="1000" height="500" alt="Image" src="https://github.com/user-attachments/assets/4810487e-1dc2-4fcf-9771-426968e0c036" />

```bash
 app_requests_total{method="GET", endpoint="/"} 120
```
Breakdown:

| Component | Meaning |
|---| ----|
| Metric Name | app_requests_total |
| Labels | method="GET", endpoint="/" |
| Value | 120 |
| Timestamp | automatically added |
