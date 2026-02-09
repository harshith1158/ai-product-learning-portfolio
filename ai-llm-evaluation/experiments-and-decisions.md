# Experiments & Product Decisions

## Objective
Improve response accuracy and reduce hallucinations without increasing latency or unnecessary escalations.
## Experiment 1: Guardrails Impact

Hypothesis:
Adding explicit unknown-intent fallback will reduce hallucinated responses.

Setup:
- Control: Original prompt without unknown-intent handling
- Variant: Updated prompt with intent guardrails and fallback
- Sample size: 10–15 representative queries
- Metrics tracked: Hallucination rate, escalation rate, user clarity

Result:
- Hallucination rate decreased
- Escalation rate slightly increased
- User clarity improved

Decision:
Accept tradeoff. Prefer safe escalation over incorrect confidence.
## Metrics Drift Observed

Observed Issues:
- Increase in escalations after guardrails
- Slight increase in response time
- Decrease in incorrect confident answers

Analysis:
Guardrails shifted behavior from overconfident automation to safer human handoff.
This is acceptable for early-stage MVP focused on trust and compliance.
## Product Decision Log

| Decision | Reason | Alternatives Considered | Final Choice |
|--------|--------|-------------------------|-------------|
| Increase escalations for unknown queries | Prevent hallucinations | Allow AI guesses | Escalate to human |
| Add latency tolerance (+0.5s) | Safety checks added | Skip validation | Keep checks |
| Limit AI scope in billing | Compliance risk | Partial automation | Human-only |
## Next Iterations (If Live with Users)

- Introduce confidence threshold tuning to reduce unnecessary escalations
- Segment intents by business value and risk
- A/B test stricter vs relaxed fallback messaging
- Add agent feedback loop to retrain intent classifier
## Executive Summary

This evaluation demonstrated that improving AI safety and trust often increases operational cost in the short term. As a product decision, I prioritized correctness and user trust over aggressive automation. This aligns with long-term product health and compliance requirements.
