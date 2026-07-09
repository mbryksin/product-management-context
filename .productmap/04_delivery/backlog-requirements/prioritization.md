# Prioritization

**Competency:** Strategy

## Summary

Systematically compare options and decide what to build or do next, using criteria and frameworks that fit the context. Good prioritisation is transparent, revisable, and defensible to stakeholders.

## Key Concepts

### Criteria-Based Prioritization

Never prioritise by gut feel or loudest stakeholder alone. Always make explicit the criteria you are using and why.

Common criteria:
- **Value** — how much does this benefit users or the business?
- **Effort** — how long will this take to build and ship?
- **Confidence** — how certain are we this will have the stated impact?
- **Risk** — what happens if we are wrong or it fails?

### RICE Scoring

RICE (Reach, Impact, Confidence, Effort) produces a numeric score that enables comparison across diverse items.

**Formula:** `(Reach × Impact × Confidence) / Effort`

| Factor | Definition | Scale |
|--------|-----------|-------|
| **Reach** | Users affected per quarter | Estimated number |
| **Impact** | How much it moves the metric | 3=massive, 2=high, 1=medium, 0.5=low, 0.25=minimal |
| **Confidence** | How sure you are about Reach and Impact | 100%=high, 80%=medium, 50%=low |
| **Effort** | Person-months to design, build, and ship | Estimated number |

### MoSCoW Framework

Use MoSCoW when aligning with stakeholders on scope for a specific release or quarter.

| Category | Definition |
|----------|-----------|
| **Must have** | Non-negotiable — the release fails without it |
| **Should have** | Important but not critical — include if possible |
| **Could have** | Nice to have — include only if time and capacity allow |
| **Won't have (this time)** | Explicitly out of scope for this cycle |

### Saying No

Prioritisation is not just about what to do — it is about what not to do. Communicate "not now" decisions clearly and document the reasoning in a decision log.

---

## RICE Scoring Table

| # | Item | Reach | Impact | Confidence | Effort | Score | Priority |
|---|------|-------|--------|------------|--------|-------|---------|
| 1 | [Fill in item] | [#] | [3/2/1/0.5] | [1.0/0.8/0.5] | [person-months] | [auto-calculate] | [H/M/L] |
| 2 | [Fill in item] | | | | | | |
| 3 | [Fill in item] | | | | | | |
| 4 | [Fill in item] | | | | | | |
| 5 | [Fill in item] | | | | | | |

---

## MoSCoW for Current Release

**Release / Cycle:** [Fill in: e.g., Q3 2025 — Activation sprint]

| Must have | Should have | Could have | Won't have |
|-----------|------------|------------|-----------|
| [Fill in] | [Fill in] | [Fill in] | [Fill in] |

---

## Decision Criteria

[Fill in: what are the strategic filters you apply before scoring? e.g., "Items must advance the activation theme", "Items must be completable in one sprint"]

1. [Criterion 1]
2. [Criterion 2]
3. [Criterion 3]

## Related

- [backlog-requirements.md](./backlog-requirements.md)
- [../../08_frameworks/rice.md](../../08_frameworks/rice.md)
- [../../01_strategy/mvp-roadmap/roadmap.md](../../01_strategy/mvp-roadmap/roadmap.md)
