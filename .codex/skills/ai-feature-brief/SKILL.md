# AI Feature Brief — AI PRD + Prompt Spec

## Name

`ai-feature-brief` — pick an AI use case and draft an AI PRD + prompt spec (value, data, risks, evaluation).

## When to use

- You need to decide *what* AI feature to build and why (value + feasibility + risk).
- You need a concrete AI PRD (requirements, UX, data, guardrails, rollout) before discovery/build.
- You need a prompt spec suitable for engineering implementation and evaluation.
- You need an evaluation plan (offline + online) and a safety/red-team checklist.

## Inputs (ask user for these)

- Product / area:
- Target users / segment:
- Current workflow / pain points (what users do today):
- Candidate AI use cases (optional; if blank, propose 3–5):
- Constraints:
  - Regions / languages:
  - Latency / cost envelope:
  - Allowed data types (PII? PHI? PCI?):
  - Tooling constraints (model hosting, vendors, runtime, devices):
  - Policy/compliance constraints:
- Data context:
  - Data sources available today (repo paths, systems, owners):
  - Data that is *not* available / not allowed:
  - Logging/telemetry available (events, warehouses):
- Timeline (absolute dates, `YYYY-MM-DD`):
  - Discovery start:
  - Target MVP date:
  - Target GA date:
- Links / context files to read (repo paths preferred):

## Outputs

- AI use case decision (selected use case + rationale + alternatives considered).
- AI PRD in Markdown (structured; explicitly references `.productmap/09_templates/ai-prd-template.md`).
- Prompt spec in Markdown (system prompt + user prompt template + inputs/outputs + eval rubric).
- Risk register + mitigations (security, privacy, safety, compliance, reliability).
- Evaluation plan (offline dataset + human eval + online experiment + launch guardrails).

## Repo knowledge to pull

- Start here (knowledge base entrypoint): `.productmap/index.md` (alias of `.productmap/INDEX.md`).
- Required template: `.productmap/09_templates/ai-prd-template.md`.
- Also consider (as relevant):
  - Templates: `.productmap/09_templates/prd-template.md`, `.productmap/09_templates/adr-template.md`, `.productmap/09_templates/user-story-template.md`, `.productmap/09_templates/persona-template.md`
  - Frameworks/tools: `.productmap/08_frameworks/`, `.productmap/07_tools/`
  - Raw inputs storage (if writing back later): `.productmap/10_data/`
  - Initiative artifacts storage (if writing back later): `.productmap/00_company/product/`

## Detailed prompt (copy/paste)

You are a senior AI Product Manager and TPM.

Goal: produce a high-quality AI Feature Brief that (1) selects the best AI use case for the product context, (2) defines user value and requirements, (3) specifies data needs and risks, (4) defines an evaluation plan, and (5) drafts an AI PRD + prompt spec that engineering can implement.

Hard constraints:
- Use absolute dates only (`YYYY-MM-DD`). Do not use “today”, “next week”, etc.
- Ground recommendations in the repository knowledge base first.
- Explicitly reference these repo paths in the “Repo sources used” section:
  - `.productmap/index.md`
  - `.productmap/09_templates/ai-prd-template.md`
- If repo templates are minimal, extend them, but still cite them as the starting point.
- Ask clarifying questions only if required to avoid wrong decisions; otherwise make reasonable assumptions and label them.

Inputs (from user):
- Product/area:
- Target users:
- Current workflow/pain:
- Candidate use cases (optional):
- Constraints (regions, latency, cost, policy/compliance):
- Data context (sources, restrictions, telemetry):
- Timeline (Discovery start, MVP, GA — all `YYYY-MM-DD`):
- Repo/context files to read (paths):

Process:
1) Summarize the problem and user goals (1 paragraph) and list any assumptions.
2) Propose 3–5 candidate AI use cases (unless user provided), each with:
   - User value and who benefits
   - Feasibility notes (data availability, integration complexity)
   - Safety/privacy risk level (low/med/high) and why
3) Choose 1 use case using a simple scoring table (Value, Feasibility, Risk, Time-to-impact; 1–5) and justify the selection.
4) Draft the AI PRD and the prompt spec for the selected use case using the output format below.

Output format (Markdown):

1. **Selected Use Case**
   - Name:
   - One-sentence summary:
   - Target users:
   - Why now:
   - Alternatives considered (and why not):

2. **AI PRD** (start from `.productmap/09_templates/ai-prd-template.md` and expand)
   - Overview
     - Problem statement
     - Goals (business + user)
     - Non-goals
     - Timeline (`YYYY-MM-DD`): Discovery, MVP, GA
   - Users & Scenarios
     - Primary persona(s)
     - Top user stories / jobs-to-be-done
     - UX entry points + example flows
   - Product Requirements
     - Functional requirements
     - Output requirements (format, tone, length, citations)
     - Performance requirements (latency, availability)
     - Internationalization (if relevant)
   - AI/ML Approach (implementation-agnostic unless user requests)
     - Task type (classification, extraction, generation, retrieval, agentic)
     - Model interaction pattern (prompt-only vs RAG vs tools/functions)
     - Context inputs (what the model sees)
     - Tool/actions the AI may take (and explicit prohibitions)
     - Fallback behavior when uncertain
   - Data Needs & Governance
     - Data sources required (each with owner, access method, freshness)
     - Training vs inference data (if applicable)
     - Labeling needs (what labels, who labels, volume estimate)
     - Privacy/compliance constraints (PII/PHI/PCI; retention; consent)
     - Logging plan (what to log, what *not* to log)
   - Risks & Mitigations (risk register table)
     - Hallucinations / incorrect output
     - Bias / fairness
     - Prompt injection / data exfiltration
     - Unsafe content
     - Privacy leakage
     - IP / copyright leakage
     - Security / unauthorized actions
     - Reliability / drift
   - Evaluation Plan
     - Offline eval: dataset plan, baselines, metrics, acceptance thresholds
     - Human eval: rubric + sampling + reviewer guidance
     - Online eval: experiment design, guardrails, stop conditions
     - Monitoring after launch: metrics, alerting, retraining/review cadence
   - Launch & Rollout
     - Beta plan and eligibility
     - Guardrails (rate limits, UI affordances, confirmations)
     - User education and disclosure
     - Support playbook / incident response triggers
   - Open Questions

3. **Prompt Spec**
   - Purpose / scope
   - Model role and boundaries (what it can/can’t do)
   - Inputs (explicit schema)
   - Output schema (prefer JSON with fields and constraints)
   - System prompt (verbatim)
   - User prompt template (verbatim, with placeholders)
   - Tool/function specs (if any) + allowed actions
   - Few-shot examples (2–3 short examples)
   - Refusal and safe-completion behavior (what to do when unsafe/unknown)

4. **Evaluation Appendix**
   - “Golden set” test cases (at least 10; include edge cases)
   - Red-team test cases (at least 10; include prompt injection attempts)

5. **Repo sources used**
   - List repo paths read and used (must include `.productmap/index.md` and `.productmap/09_templates/ai-prd-template.md`)

## Workflow (runbook)

1. Read `.productmap/index.md` and `.productmap/09_templates/ai-prd-template.md` first.
2. Read user-provided context paths; if none, search the repo for relevant terms (product name, feature area, user segment).
3. Confirm constraints and timeline (all dates must be `YYYY-MM-DD`).
4. Generate candidate AI use cases and select one with a scoring table.
5. Draft the AI PRD (expanded from the template) and the prompt spec.
6. Produce the evaluation plan and a risk register with mitigations.
7. Run the red-team/safety checklist and add gaps as explicit “Open Questions”.
8. If the user wants artifacts written back: propose a location under `.productmap/00_company/product/<initiative>/` and ask for confirmation before writing.

## Quality checklist

- Use case choice is explicit, justified, and includes alternatives.
- Clear user value: measurable improvement vs current workflow.
- Requirements are testable (acceptance criteria, thresholds, guardrails).
- Data needs are concrete (sources, access, freshness, owners, restrictions).
- Privacy/compliance is addressed (PII/PHI/PCI handling, retention, logging exclusions).
- Prompt spec is implementable (schemas, examples, refusal behavior, tool boundaries).
- Evaluation plan includes offline + human + online, with stop/rollback criteria.
- Risk register includes mitigations and residual risk callouts.
- All dates are absolute (`YYYY-MM-DD`), not relative.
- “Repo sources used” lists the repo paths consulted (must include required paths).

## Red-team / safety checklist

- Prompt injection: attempts to override system instructions; data exfiltration attempts; “ignore previous instructions”.
- Sensitive data leakage: ensure PII/PHI/PCI is not returned; define redaction and refusal behavior.
- Unauthorized actions: confirm the AI cannot perform privileged operations without explicit user confirmation and authorization.
- Overreach: prevent confident-sounding output when uncertain; require calibrated uncertainty / “needs review”.
- Hallucination traps: missing context, ambiguous entities, fabricated citations/sources.
- Toxic/unsafe content: ensure refusal/safe-completion patterns are defined and tested.
- Bias/fairness: test for disparate outcomes across user groups, languages, or names.
- Security: ensure no secrets in prompts/logs; define how to handle tokens/keys.
- Abuse and misuse: define misuse scenarios and anti-abuse guardrails (rate limits, friction, monitoring).
- Monitoring: define post-launch signals for safety regressions and incident response steps.
