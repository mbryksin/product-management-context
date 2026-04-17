---
name: user-research-interviews
description: Use this skill when the user is planning, running, or synthesizing user research — especially discovery interviews, problem interviews, solution interviews, usability tests, or JTBD interviews. Triggers — "user interviews", "customer discovery", "needfinding", "interview guide", "synthesize interviews", "JTBD interview", "Mom Test", "usability test".
---

# User research interviews

Use this skill when the work is **qualitative, conversational, and participant-led** learning about problems, contexts, mental models, jobs, or how people use (or fail to use) a product. Prefer it over improvised “chat with users” scripts that bias toward validation, demos, or selling.

## When this skill applies (and when it does not)

**Applies when**

- You need **thick context**: why something matters, what “good” looks like, what workarounds exist, what triggers a switch.
- You are in **discovery** (problem/needfinding), **solution/concept** testing, **usability** evaluation, **JTBD** exploration, or **win/loss** reconstruction.
- You must produce **actionable insight** for product decisions (scope, positioning, UX, roadmap), not just anecdotes.

**Does not replace (delegate instead)**

- **Surveys** when you need representative prevalence, segmentation at scale, or statistically bounded estimates. Interviews inform survey design; surveys validate scale.
- **Analytics** when the question is “what happened” in production with large samples. Pair analytics (what) with interviews (why).
- **Strategy-only** questions (vision, portfolio bets) where executive judgment and market models dominate; interviews **inform** strategy but do not substitute for it.
- **Sales calls** or **support tickets** as primary evidence when the goal is pipeline or ticket resolution; mine them for hypotheses, then run dedicated research.

## Interview types (goal, when, structure)

Use one primary interview type per session. Mixing problem discovery and a polished demo in one hour usually corrupts both.

### 1) Problem / discovery interviews

- **Goal**: Understand pains, goals, workflows, constraints, and what people already do today (including “do nothing” and hacks).
- **When**: Early stage, new segment, after a strategy shift, when metrics moved but causes are unknown.
- **Structure**: Warm-up → context mapping (a day in the life / workflow) → deep dives on recent concrete episodes → trade-offs and priorities → wrap (consent, follow-ups).

### 2) Solution / concept interviews

- **Goal**: Test comprehension, perceived value, objections, and fit of a proposed approach (not “do you like it?”).
- **When**: After you understand the problem; before committing build; when positioning or packaging is uncertain.
- **Structure**: Re-anchor the problem in their words → show stimuli in **small chunks** (storyboard, prototype narrative, pricing frame) → probe reactions with **comparables** and **trade-offs** → capture dealbreakers and “must be true” assumptions.

### 3) Usability tests (task-based)

- **Goal**: Observe whether representative users can accomplish realistic tasks with acceptable friction and comprehension errors.
- **When**: Any time UI changes risk core flows; before launch; when funnels show drop-offs.
- **Structure**: Scenario setup → **think-aloud** or retrospective prompts → task list with success criteria → severity-tagged issues → debrief on mental model mismatches.

### 4) JTBD “switch” interviews

- **Goal**: Reconstruct the timeline of how someone moved from an old approach to a new one; identify forces (push/pull, anxiety, habit) and hiring/firing criteria.
- **When**: Category creation, repositioning, onboarding redesign, churn analysis, packaging/pricing research.
- **Structure**: Identify the job statement collaboratively → map **first thought** → passive looking → active looking → deciding → onboarding → ongoing use → churn/rehire moments.

### 5) Win / loss interviews

- **Goal**: Explain purchase decisions in the buyer’s organizational and competitive context; separate “product gaps” from “process/politics/timing.”
- **When**: Pipeline reviews, competitive pressure, enterprise deals, renewal risk.
- **Structure**: Decision criteria → evaluation timeline → alternatives considered → proof required → stakeholders → what would have changed the outcome.

## The Mom Test — three rules (verbatim-style)

These rules reduce polite agreement and fantasy futures:

1. **Talk about their life instead of your idea.**
2. **Ask about specifics in the past instead of generics or opinions about the future.**
3. **Talk less and listen more.**

Operationalize them by asking for **the last time** something happened, **what they did before and after**, **what they paid** (money, time, political capital), and **what almost stopped them**.

## Workflow — planning (numbered)

1. **Decide the decision** this research must inform (one sentence). If you cannot name the decision, narrow scope.
2. **Pick the interview type** (see above). Write a one-paragraph **research question** and **anti-goals** (what you will not claim from this method).
3. **Define the participant filter** (role, situation, recency, authority). Prefer people who **recently** experienced the problem or workflow.
4. **Draft a guide** (see artifact skeleton). Pilot internally; trim to fit the timebox with buffer for tangents that matter.
5. **Logistics & ethics**: consent, recording policy, incentives, data handling, PII minimization, and how notes will be stored (see cross-refs under `10_data/`).
6. **Assign roles** if paired: interviewer vs note-taker; debrief cadence; shared tagging vocabulary.

## Workflow — running (rules)

1. **Open with safety and purpose**: what you are learning, how notes are used, opt-out on any question.
2. **Ask one question at a time**; tolerate silence; avoid stacking prompts.
3. **Anchor on behavior**: “Walk me through…” beats “How do you usually…?” when followed by a recent example.
4. **Never pitch** in a discovery session; if you demo, do it **after** you have captured their unprompted framing.
5. **Mirror language**; do not “correct” them into your taxonomy until synthesis.
6. **Probe with gentle ladders**: “What happened next?” “What did that cost you?” “Who else was involved?”
7. **Watch for peak moments** (delight, shame, fear, urgency); those are where requirements hide.
8. **Close with meta**: “What should I have asked?” “Who else experiences this?” “May I follow up?”
9. **Debrief within 24 hours** while memory is fresh; capture **verbatim quotes** only when useful and permitted.
10. **Track quality signals**: rich episodes vs vague opinions; contradictions to revisit next session.

## Workflow — synthesizing

1. **Tag raw notes** with a small controlled vocabulary (e.g., `pain`, `workaround`, `goal`, `constraint`, `objection`, `delight`, `terminology`, `workflow`, `stakeholder`, `tool`, `metric`).
2. **Extract atomic observations** (single idea per note card/slip).
3. **Affinity map** into emergent themes; let clusters rename themselves from participant language.
4. **Write an insight brief** per theme: observation → interpretation → implication → confidence (High/Med/Low) → recommended next step (design change, experiment, more research).
5. **Separate evidence from recommendations** so stakeholders can disagree with your read without erasing data.
6. **Quantify only what interviews support**: counts of **mentions** across a sample, not population prevalence.

## Evidence ladders (turn opinions into episodes)

Use a repeatable ladder so “I think / I usually / I would” becomes inspectable behavior:

1. **Topic frame** (neutral): “When you’re responsible for X, what tends to go wrong?”
2. **Recency filter**: “When did that last happen?” (must be recent enough to remember details)
3. **Scene setting**: “Where were you, what were you trying to accomplish, who was waiting on you?”
4. **Step-by-step**: “What did you try first / next?” (surface workarounds and toolchains)
5. **Costs**: time, money, rework, reputation, political capital, risk
6. **Comparison**: “What else did you consider?” (competitors are spreadsheets, humans, inertia)
7. **Decision rule**: “How will you decide next time?” (only after the episode exists)

If you cannot reach step 3, you do not yet have usable evidence—either change participants (wrong filter) or change prompts (too abstract).

## Probe banks (examples; adapt to domain)

**Problem / discovery**

- “Tell me about the last time `<painful workflow>` went sideways.”
- “What did you do immediately before and after?”
- “What tools touched that workflow?”
- “Who had to approve or unblock you?”
- “What would ‘good enough’ look like in that moment?”

**Solution / concept**

- “Before I show anything: how do you solve this today?”
- “I’m going to show `<stimulus>` in two parts. After each part, tell me what you think it is for, in your own words.”
- “Compared to `<status quo>`, what becomes easier or harder?”
- “What would make you reject this outright?”
- “What proof would you need to trust it?”

**Usability**

- “Please think aloud as you go; I care about confusion, not ‘right answers’.”
- “If you were really doing this for work, what would you click next?”
- “Stop when you believe you’re done; tell me whether you’re confident.”
- “What did you expect to happen after that click?”

**JTBD switch**

- “When did you first realize the old way wasn’t good enough?”
- “What were you doing the day you started searching?”
- “What almost kept you from switching?”
- “What had to be true for you to feel safe onboarding?”

**Win / loss**

- “Walk me through the evaluation timeline from first interest to signature.”
- “Who could veto this, and did they?”
- “Which alternatives were seriously considered, not just mentioned?”
- “If we replayed the quarter, what one variable changes the outcome?”

## Note-taking template (per session)

Capture **timestamped** bullets (or approximate segments) so synthesis can trace claims:

- **Participant descriptor** (role, segment, relevant context) — avoid unnecessary PII in shared notes
- **Tasks / topics covered** vs skipped (time overruns)
- **Verbatim snippets** (only if consented and necessary)
- **Observed behaviors** (hesitations, workarounds, misunderstandings)
- **Hypotheses generated** (label as `H:` so they are not treated as facts)
- **Follow-ups** (questions to ask next participant)

If paired, the note-taker owns structure; the interviewer owns rapport and follow-ups.

## Recruitment, incentives, and saturation

**Recruitment quality** dominates outcome quality. Prefer:

- **Recency**: people who did the workflow in the last 30–90 days (tune to domain cadence)
- **Authority**: for B2B, include both **doers** and **economic buyers** when decisions split
- **Diversity of context**: different company sizes, stacks, regions, maturity—until themes repeat

**Incentives** should match effort and professional norms (cash, gift cards, charity donation, enterprise swag policy). Disclose incentives in the session contract.

**Saturation** signals (stop when several are true):

- New sessions mostly **relabel** old themes without adding mechanisms
- **Surprising** failures to appear after widening recruitment filters
- You can **predict** participant stories halfway through the arc (still validate, but diminishing returns)

Saturation is not a magic number; document your stopping rule before you start.

## Usability specifics (beyond generic interviewing)

- Write **tasks** as scenarios (“You need to…”) not leading instructions (“Click Reports”).
- Define **success criteria** per task (completion, correctness, time threshold if relevant).
- Tag issues with **severity** (e.g., blocker / major / minor / cosmetic) and evidence (quote + observation).
- Separate **UI defects** from **information architecture** problems; fixes differ.
- Run **5–8** participants per homogeneous user group for many consumer patterns; enterprise may need more roles.

## Triangulation (pair interviews with other repo signals)

Use interviews to explain signals from:

- **Analytics** funnels and event sequences (form hypotheses from numbers, test with episodes)
- **Support tickets** and **CS notes** (mine for recurring failure modes)
- **Sales objections** (validate whether objections are product gaps vs buying process artifacts)

In the synthesis doc, add a short **triangulation table**: signal → what interviews clarified → remaining uncertainty.

## Pitfalls (common failure modes)

1. **Leading with the solution** (“Would you use a dashboard that…?”) produces performative yes.
2. **Hypothetical futures** (“Would you pay…?”) are weak evidence; reconstruct past wallet and effort instead.
3. **Friendly expert interviews** where you talk 60% of the time; you leave with your slides, not their reality.
4. **Overfitting to last interview**; maintain a rolling synthesis after every N sessions.
5. **Mixing multiple jobs** in one guide (sales + UX + strategy); you get shallow coverage of each.
6. **Ignoring non-users** and **successful non-consumption**; the best competitor is often inertia.
7. **Synthesis theater**: themes without quotes/behavioral anchors; stakeholders cannot trust it.
8. **Ethics drift**: sharing identifiable quotes internally without consent boundaries.

## Questions to ask the user before drafting artifacts

1. What **decision** must this research inform, and by what date (`YYYY-MM-DD`)?
2. Which **interview type** is primary, and who is **in/out** of scope as a participant?
3. What **constraints** exist (B2B procurement, regulated domains, no recording)?
4. What **artifacts or prototypes** will be shown, if any, and in what order?
5. How many sessions are planned, and what **saturation** signal will stop recruitment?
6. Where should raw notes live in the repo (path under `10_data/`)?
7. What **language/market** nuances should the guide respect?
8. What **prior beliefs** are you willing to falsify with negative evidence?

## Artifacts

### Interview guide — five-section skeleton

1. **Research intent & session contract** (purpose, time, recording, confidentiality).
2. **Warm-up & context** (role, environment, recent relevant activity).
3. **Core arc** (episodes, workflows, comparisons, trade-offs) aligned to the interview type.
4. **Stimuli block** (only if needed): show → task → debrief prompts; include failure probes.
5. **Close & logistics** (follow-ups, intros, incentives, thank-you).

### Synthesis template (Markdown)

- Title: `<Initiative> — Interview synthesis — YYYY-MM-DD`
- `Decision being informed`
- `Methods & sample` (who, n, dates)
- `Key themes` (each: bullets + supporting quotes/behaviors + confidence)
- `Implications for product` (separate from evidence)
- `Open questions / next research`
- `Appendix: tag dictionary & affinity cluster notes`

### JTBD timeline sketch (blank)

- **First thought** → **passive looking** → **active looking** → **deciding** → **onboarding** → **habit** → **switch away / rehire**
- For each stage: triggers, anxieties, habits, evidence sought, who influenced, what almost blocked progress.

## Repo cross-references (read before writing)

- `.productmap/02_generation/user-research/_overview.md`
- `.productmap/08_frameworks/jobs-to-be-done.md`
- `.productmap/09_templates/persona-template.md`
- `.productmap/10_data/interviews/` (store structured notes and guides when used)
- `.productmap/10_data/feedback/` (adjacent raw signals; triangulate)

Navigation entrypoint when unsure where content lives: `.productmap/index.md`.

## Conventions

- Label artifacts with **absolute dates** (`YYYY-MM-DD`).
- Initiative-specific writeups belong under `.productmap/00_company/product/` unless the user specifies otherwise; raw inputs under `.productmap/10_data/`.

## Quality bar

- Guides produce **behavioral evidence**, not opinion polls.
- Synthesis states **confidence** and **next validation** for each major claim.
- Recommendations trace to **observations** stakeholders can audit.
