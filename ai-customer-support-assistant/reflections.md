Reflections : This section captures learning, risks, and continuous improvement opportunities.

Risks & considerations:
- Data quality: garbage in -> garbage out. Ensure KB and transcript cleanliness.
- Model drift: ongoing monitoring and refresh cycles are necessary.
- Over-reliance: avoid routing all tasks to the model without human oversight for sensitive cases.
- Privacy: strict handling of PII and contractual obligations for data sent to third-party APIs.

What to learn from the pilot:
- Which query types are most defeatable by automation.
- How agents use and correct suggestions — measure acceptance and friction.
- Real-world hallucination patterns and how to reduce them.

Next experiments:
- A/B test different prompt templates and grounding strategies.
- Compare embeddings models and vector DB configurations for recall/latency tradeoffs.
- Experiment with small-scale fine-tuning on high-value intents.

Maintenance:
- Schedule regular data syncs, embedding refreshes, and model performance reviews.
- Set clear ownership for KB curation and incident response.
