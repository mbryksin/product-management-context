# Decision-Making

**Competency:** Facilitation

## Summary

Use clear process and criteria so the right people are involved and decisions are documented and communicated. Good decision-making practices prevent revisited debates, speed up alignment, and build organisational trust.

## Key Concepts

### Decision Rights and RACI

Clarify who does what before making significant decisions.

| Role | Meaning |
|------|---------|
| **Responsible** | Does the work to make the decision |
| **Accountable** | Final authority — only one person per decision |
| **Consulted** | Input is sought before the decision is made |
| **Informed** | Notified after the decision is made |

Use RACI to prevent ambiguity about who has the final call.

### Options, Criteria, and Trade-offs

For any significant decision:
1. Define the options (at least two, ideally three — including "do nothing")
2. State the criteria for evaluation (e.g., user impact, engineering effort, reversibility)
3. Assess each option against the criteria
4. State the trade-offs explicitly — who or what benefits and who or what loses

### Documenting and Communicating Decisions

Log every significant product decision. A decision log:
- Prevents relitigating past decisions
- Onboards new team members faster
- Creates accountability and clarity on rationale

For high-stakes decisions, write an ADR (Architecture Decision Record) — see `09_templates/adr-template.md`.

---

## Decision Log

| Date | Decision | Options Considered | Rationale | Owner | Status | Link |
|------|----------|--------------------|-----------|-------|--------|------|
| [YYYY-MM-DD] | [Fill in: what was decided] | [Fill in: what alternatives were considered] | [Fill in: why this option was chosen] | [Name] | [Decided / Pending / Revisited] | [Link to doc or ticket if relevant] |
| | | | | | | |
| | | | | | | |

---

## Decision Framework for Complex Choices

When a decision is high-stakes or contested, use this structure:

**Decision:** [Fill in: what needs to be decided, and by when]

**Accountable:** [Fill in: who has final authority]

**Options:**

| Option | Pros | Cons | Risk |
|--------|------|------|------|
| [Option A] | [Fill in] | [Fill in] | [Fill in] |
| [Option B] | [Fill in] | [Fill in] | [Fill in] |
| [Option C: Do nothing] | [Fill in] | [Fill in] | [Fill in] |

**Recommended:** [Fill in: which option and why]

**Decision:** [Fill in: what was ultimately decided and by whom]

## Related

- [communication.md](./communication.md)
- [workshops.md](./workshops.md)
- [../../04_delivery/backlog-requirements/prioritization.md](../../04_delivery/backlog-requirements/prioritization.md)
- [../../09_templates/adr-template.md](../../09_templates/adr-template.md)
