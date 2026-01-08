AI Design

High-level architecture:
- Channels: chat widget, email, help center search, internal agent UI.
- API layer / Orchestration: receives requests, enforces auth, invokes pipeline.
- Retrieval layer: embeddings pipeline (text -> vector store), retriever, relevance scoring.
- LLM Layer: generation with prompt templates, system instructions, and citations.
- Safety & Post-processing: response filters, hallucination checks, PII redaction.
- Agent UI: show suggested replies, top sources, similarity scores, and edit controls.
- Observability: logs, metrics, and lineage for auditability.

Key design choices:
- Use RAG to ground responses; always return source snippets and links.
- Start with an open or hosted LLM (e.g., OpenAI GPT-family or private model) and plan to experiment with fine-tuning.
- Embeddings: update nightly or on content changes; store vectors in a managed vector DB (e.g., Milvus, Pinecone, or Weaviate).
- Prompts: maintain prompt templates with explicit instructions to cite sources and avoid fabricating facts.
- Safety: apply classifiers for PII, toxicity, and policy violations before returning content.

Mitigations for hallucination and unsafe outputs:
- Return top-k source snippets and include inline citations.
- If confidence is low, escalate to human agent or reply with a safe fallback.
- Keep deterministic rules for sensitive categories (billing, account closure, legal advice) to route to agents only.

Privacy & compliance:
- Redact PII before sending data to third-party models where required.
- Keep an encrypted audit trail of prompts, responses, and sources for compliance.
