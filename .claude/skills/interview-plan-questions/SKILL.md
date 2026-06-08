---
name: interview-plan-questions
description: Generate a tailored interview question set for either founder customer discovery (pre-PMF) or UX / needfinding interviews. First collects product context, hypothesis, and user segment, then produces a structured 30–60 minute question guide.
user-invocable: true
argument-hint: "[optional: interview type and topic]"
---

# Interview Plan: Question Generator

Use this skill when the user needs a structured set of interview questions for customer discovery or UX research.

## When to Use

- Preparing for founder customer interviews before product-market fit.
- Running UX or needfinding interviews to understand user behavior and pain points.
- Building a 30–60 minute interview guide grounded in a specific product hypothesis and user segment.

---

## Step 1 — Collect Context (Always Do This First)

Before generating any questions, ask the user all of the following. Do not skip this step.

Present these as a single message with 5 numbered questions:

1. **Interview type** — Which type of interview are you preparing?
   - A) Founder customer discovery (pre-PMF): understanding whether a problem is real, severe, and worth solving
   - B) UX / needfinding: understanding how users behave today, where workflows break, and what they actually need

2. **Product / problem area** — Describe in 1–3 sentences what you are building or what problem space you are exploring. What is the core activity or workflow you want to learn about?

3. **Hypothesis** — What do you currently believe is true about the user's problem, behavior, or need? Complete this sentence: *"We believe [user type] has [problem] and currently solves it by [current behavior], and the riskiest unknown is [X]."*

4. **User segment** — Who are you going to interview? Include:
   - Role or job title
   - Company type, industry, or context (if relevant)
   - Any known behavior signals (e.g. "they use spreadsheets for X", "they manage a team of 5+")

5. **Interview length** — How long is the session? (30 minutes or 60 minutes)

Wait for the user's answers before proceeding to Step 2.

---

## Step 2 — Generate the Interview Guide

Use the answers to tailor the guide. Apply the appropriate template below based on interview type.

### Time Allocation Rules

**30-minute interview:**
- Opening and warm-up: 5 min
- Core discovery questions: 18 min
- Severity / alternatives check: 5 min
- Closing: 2 min

**60-minute interview:**
- Opening and warm-up: 7 min
- Core discovery questions: 30 min
- Severity / alternatives / buying check: 15 min
- Deep-dive or magic wand: 5 min
- Closing: 3 min

Adjust the number of questions to fit the time. Do not produce more questions than can realistically be covered. Mark each section with its time budget.

---

## Template A — Founder Customer Discovery (Pre-PMF)

Apply The Mom Test principles throughout. Ask about past behavior, not future intent. Never ask whether the user likes the idea. Never pitch early.

### Opening (5 min / 7 min)

Use a casual, non-pitchy framing:

- "I'm trying to understand how people deal with [problem area] today. Not selling anything — just learning."
- "There are no right answers. I'm especially interested in what's annoying, broken, or not worth solving."

**Warm-up questions** (tailor [X] to the product area):
- "Tell me about your role and what a typical week looks like."
- "How does [relevant workflow] fit into your day-to-day responsibilities?"
- "What are you responsible for when it comes to [problem area]?"

### Getting to Know Their World (use 2–3, tailor to segment)

- "Tell me about your experience with [X activity]."
- "Tell me about your relationship with [X problem]."
- "What does a typical [day / week] look like when [X situation] comes up?"
- "What tools or processes are you using most often for [X]?"

### Core Discovery — Problem and Behavior

Lead with the riskiest unknown from the user's hypothesis. Use specific past behavior, not hypotheticals.

**Problem and frequency:**
- "Walk me through how you currently handle [problem area] — from the beginning."
- "When was the last time this came up? What happened?"
- "What triggered it? Who was involved?"
- "How often does this happen?"
- "What's the hardest part about [X activity]?"
- "What part of [X process] do you dread most?"
- "What could be easier about [X task]?"

**Current behavior and workarounds:**
- "What tools, spreadsheets, people, or processes do you use for [X]?"
- "What's your current process for completing [X task]? Walk me through each step."
- "How did you choose that approach?"
- "What else did you try before this?"
- "Why did you stop using the previous solution?"
- "Have you created any workarounds to solve [X problem]?"

**Digging in:**
- "What's your biggest pain point with [X activity]?"
- "What do you like about [X activity]?"
- "What do you dislike about [X activity]?"
- "How much time do you currently spend on [X activity]?"
- "How much time or money have you spent trying to solve [X problem]?"

### Severity Check

You need to know whether the problem is painful or merely interesting.

- "What does this cost you — in time, money, stress, or missed outcomes?"
- "What happens if this doesn't get fixed?"
- "Has this ever caused a missed deadline, lost customer, revenue loss, or team conflict?"
- "Where does this sit among your current priorities?"
- "What's your team's current budget for [X activity]?"
- "Have you already spent money trying to solve this?"
- "Is anyone actively looking for a better solution?"

### Buying and Decision-Making (B2B or team context)

Include these when the product is B2B or requires team adoption:

- "Who would need to approve a change to this process?"
- "Who pays for tools in this area?"
- "Tell me about the last tool your team bought for something similar."
- "How did that buying process work?"
- "What would make a new solution impossible to adopt?"
- "Who else should I speak with to understand this properly?"

### Closing

- "Who else should I talk to about this?"
- "Is there anything I should have asked but didn't?"
- "Would you be willing to [look at a prototype / review a draft / connect me with your ops lead] next week?"

---

## Template B — UX / Needfinding Interview

Apply needfinding principles. Focus on current behavior and real workflows. Avoid asking users to predict what they would do with a future design. Move from broad to specific using the funnel technique.

### Opening (5 min / 7 min)

Set expectations clearly:

- "Thanks for joining. I'm trying to understand how people currently handle [workflow]. There are no right or wrong answers — I'm here to listen, not to test you."
- "We'd like to record for note-taking only. You can skip any question and stop at any time."

**Warm-up questions:**
- "Tell me a bit about your role and what a normal week looks like."
- "How does [this area of work] fit into your responsibilities?"
- "Walk me through the current process."

### Questions About Behavior

Anchor the interview in real, recent experience:

- "Tell me about the last time you had to [do this task / handle this situation]."
- "Walk me through what happened from the beginning."
- "What kicked it off? Who was involved?"
- "What tools did you use?"
- "How often does this come up?"
- "How long does it usually take?"
- "What breaks when this goes badly?"

### Questions About the Problem

Identify friction, uncertainty, and breakdowns:

- "What part of that process felt hardest?"
- "Where did things slow down, break down, or become frustrating?"
- "What made that difficult?"
- "What did that cost you — in time, confidence, effort, or outcome?"
- "What problems do you experience most often when doing [X]?"
- "What's the hardest part about [X activity]?"

### Questions About Motivation

Understand why the problem matters enough to change:

- "Why was solving that important to you?"
- "What happens if it doesn't get solved well?"
- "How do you know the outcome was good enough?"
- "Who notices when this goes wrong?"

### Questions About Alternatives and Workarounds

Current alternatives reveal the true competition and the trade-offs people already accept:

- "How do you handle this today?"
- "What tools or processes do you use to solve [X problem]?"
- "What have you tried before? Why did you stop?"
- "What's good enough about the current way that keeps you from switching?"
- "What's missing from what you use today?"
- "Have you created any workarounds?"

### Probing Techniques

Use these throughout to go deeper:

- **Mirroring:** Repeat the participant's last few words in a questioning tone to invite elaboration.
- **Five Whys:** "You mentioned [X]. Why is that important for you?" Repeat to uncover motivation.
- **Labeling:** "It sounds like the issue is less about [X] and more about [Y] — is that right?"
- **Anchoring:** "Can you give me a specific example?" / "When did that last happen?" / "What did you do?"

### Magic Wand (60 min only, use after deep behavior exploration)

- "If you could change anything about this process, what would you change first?"

Use sparingly. Only after exploring current behavior in depth.

### Wrap-Up

- "What did I not ask that I should have asked?"
- "Who else should I speak with about this topic?"
- "If this problem were solved well, what would change for you?"

---

## Question Quality Checklist

Before finalising the guide, verify each question:

- Does it ask about their life, not your idea?
- Does it ask about specific past behavior, not future intent?
- Could they answer honestly without trying to please you?
- Does it avoid mentioning the product too early?
- Does it help test a risky assumption?
- Does it invite a story, example, or real workflow?
- Can you follow up with "Tell me about the last time that happened"?

If the answer to any of these is no, rewrite the question.

### Questions to Avoid

| Avoid | Use instead |
|---|---|
| "Do you like our idea?" | "How do you currently handle this?" |
| "Would you use this?" | "When was the last time you had this problem?" |
| "Would you pay $X/month?" | "What do you currently pay to solve this?" |
| "What features do you want?" | "What are you trying to accomplish when you ask for that?" |
| "Is this a big problem?" | "What happened the last time this caused trouble?" |
| "Would this save you time?" | "How long does this take today?" |
| "Is reporting frustrating?" | "What parts of the workflow are most frustrating, if any?" |
| "Do you also hate doing this manually?" | "How does this step work today? Which parts are manual?" |

---

## Output Format

Produce the final guide as a single Markdown document with the following structure:

```markdown
# Interview Guide — [Interview Type] — [YYYY-MM-DD]

## Context
- Product / problem area: ...
- Hypothesis: ...
- Segment: ...
- Interview length: ...

## Riskiest Unknowns
- (3 bullets drawn from the hypothesis)

## Interview Flow

### Opening (X min)
[questions]

### [Theme 1] (X min)
[questions with optional probe notes]

### [Theme 2] (X min)
...

### Closing (X min)
[questions + next step ask]

## Post-Interview Debrief (fill after each session)
- Signals of pain:
- Signals of urgency:
- Current alternatives mentioned:
- Language / words the participant used:
- What surprised you:
- Questions to revise for next time:
```

Print the guide in full. Do not summarise or abbreviate the questions. Make every question immediately usable in a real interview.

---

## Red Flags to Brief the Interviewer On

Include a short "Watch out for" block at the end of the guide:

- You are talking more than they are — stop and ask a question.
- They are complimenting the idea instead of describing their life — deflect with "Can you give me a specific example?"
- They are speaking in generalities ("usually", "always", "everyone") — anchor with "When did that last happen?"
- You feel reassured but have no concrete facts — the questions were too safe.
- You leave without a clear next step — always end with a commitment ask or referral.
