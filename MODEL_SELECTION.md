## the champion
Picked `logreg` (MLflow `churn-model` version 1) with `f1 = 0.495` and `p95 = 10.8 ms`, well within the latency budget and promoted as the initial champion.

## My promotion rules
- Latency budget (p95): `25.0` ms, because `10.8 ms` is comfortably fast for real-time inference with margin.
- Minimum gain to replace the champion (F1 points): `0.005`, because it prevents replacing the champion for negligible noise.

## What I would check next
Data drift in `churn_v2.csv` or underperforming customer slices (such as specific contract types) in production.
