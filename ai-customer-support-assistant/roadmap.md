Roadmap : This roadmap outlines a phased delivery plan aligned with business goals and technical readiness.

Phase 0 — Discovery & Data Collection (Weeks 0–2)
- Inventory sources: KBs, transcripts, ticketing system, product docs.
- Define success metrics and baselines.
- Export sample data and sanitize PII.

Phase 1 — MVP (Weeks 2–6)
- Implement RAG pipeline with an embeddings store and retriever.
- Simple agent UI and public API endpoints.
- Basic intent classifier and routing rules.
- Metrics dashboard for FRT, deflection, and CSAT.
- Acceptance criteria: 30% deflection on repetitive queries, <2s median retrieval latency, end-to-end demo.

Phase 2 — Improve & Scale (Weeks 6–12)
- Fine-tune LLM responses or set up instruction prompts for consistency.
- Add connectors (Zendesk, Intercom, Salesforce) and channel support.
- Build active learning loop to capture corrections.
- Improve latency, caching, and cost optimization.

Phase 3 — Production & Compliance (Weeks 12–20)
- Harden security, monitoring, SLOs, and automated alerts.
- Establish audit logs, data retention policies, and PII redaction.
- Run pilot with a subset of customers and collect feedback.

Ongoing
- Monitor model drift, retrain or refresh embeddings, expand language coverage.
