---
name: ai-product-feature-spec
description: Specifies AI/ML product behavior, evaluation, safety, and data handling using the AI PRD template and AI/ML overviews. Use for LLM features, classification, recommendations, or prompt-based flows.
---

# AI product feature specification

## When to use

- Shipping or scoping AI-assisted user experiences, model behavior, or human-in-the-loop flows.
- Need eval criteria, fallbacks, and privacy aligned with repo templates.

## Steps

1. Read [`02_generation/ai-ml/_overview.md`](../../../.productmap/02_generation/ai-ml/_overview.md) and [`09_templates/ai-prd-template.md`](../../../.productmap/09_templates/ai-prd-template.md); cross-link to core PRD sections in `prd-template.md`.
2. Define intended behavior, failure modes, offline/online eval, logging, and red-team/safety notes appropriate to risk.
3. State training/inference boundaries and PII handling; date the spec.

## Delegation

Use [subagent-prompt.md](subagent-prompt.md) for a sub-agent that specializes in AI feature specs (plays to strong structured + prompt-design reasoning).
