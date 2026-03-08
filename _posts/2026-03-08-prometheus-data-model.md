---
title: Prometheus Data Model (Time Series + Labels)
date: 2026-03-08
---

Prometheus stores data as a time series.
A Time Series = **metric name** + **Labels** + **Timestamps** + **Value**

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
