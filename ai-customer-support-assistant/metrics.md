Metrics & Success Criteria : Metrics define how success is measured across customer experience, reliability, and business performance.

Primary metrics:
- First Response Time (FRT): median time to first meaningful response (target: <1 minute for automated responses, <15 minutes human SLA).
- Resolution Time: median time to resolution for issues solved by assistant vs. agent.
- Deflection Rate: percent of queries resolved by assistant without human handoff (target: 25–40% in year 1).
- CSAT / Customer Satisfaction: target improvement vs baseline.
- Suggestion Accuracy: percent of agent-assist suggestions accepted by agents (target: >70%).

Safety & reliability metrics:
- Hallucination Rate: percent of responses flagged for incorrect or ungrounded facts (target: <2–5%).
- PII Leakage Incidents: count of incidents where PII left unredacted (target: 0).
- Latency: 95th percentile end-to-end response latency (target: <3s for retrieval+generation).

Operational metrics:
- Throughput: queries per minute supported.
- Cost per resolved query.
- Model inference cost and embedding update frequency.

Monitoring:
- Dashboards for trends, alerts for anomaly detection (spikes in hallucinatory responses, latency, or errors).
