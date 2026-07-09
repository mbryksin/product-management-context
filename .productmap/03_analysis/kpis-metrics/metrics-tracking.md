# Metrics Tracking

**Competency:** Delivery

## Summary

Define, track, and report metrics that show whether product and team outcomes are being achieved. Good metrics tracking connects daily work to strategic goals and surfaces problems before they become crises.

## Key Concepts

### North Star and Supporting Metrics

- **North Star Metric (NSM):** the single metric that best captures the core value your product delivers to users. Leading indicator of long-term revenue.
- **Supporting metrics:** 3–5 metrics that drive or explain the NSM. One per strategic theme or team.
- **Counter-metrics:** guardrail metrics that flag if optimising the NSM creates unintended harm (e.g., quality drops while quantity rises).

### Leading vs. Lagging Indicators

| Type | Description | Example |
|------|-------------|---------|
| **Leading** | Predictive — changes before outcomes do | Daily active users, feature adoption rate |
| **Lagging** | Confirming — measures outcomes after the fact | Monthly revenue, annual churn rate |

Use both: leading indicators help you act in time; lagging indicators confirm results.

### Dashboards and Reporting Cadence

- **Daily:** engineering and delivery health (error rates, deploy frequency)
- **Weekly:** product usage and activation metrics; team reviews blockers
- **Monthly:** leadership review of NSM progress against OKRs
- **Quarterly:** full metric audit and OKR scoring

---

## North Star Metric

**NSM:** [Fill in: the one metric that best captures value delivered to users]

**Definition:** [Fill in: precise definition — what counts, what doesn't, how it is calculated]

**Current value:** [Fill in]

**Target:** [Fill in]

**Why this metric:** [Fill in: one sentence explaining why this captures core value]

---

## Events to Track — AARRR Funnel

Replace placeholder event names with the actual events relevant to your product.

### Acquisition

| Event | Trigger | Properties |
|-------|---------|------------|
| [e.g., Landing Page Visited] | User arrives on main landing page | source, medium, campaign |
| [e.g., Signup Started] | User opens registration flow | referral_source |
| [e.g., Signup Completed] | User creates account | plan_type |

### Activation

| Event | Trigger | Properties |
|-------|---------|------------|
| [e.g., Onboarding Completed] | User finishes setup flow | steps_completed |
| [e.g., First Core Action Taken] | User performs the key value action | feature_name |
| [e.g., Aha Moment Reached] | User reaches the defined aha moment | session_number |

### Retention

| Event | Trigger | Properties |
|-------|---------|------------|
| [e.g., Weekly Active Session] | User logs in and takes action in a week | week_number |
| [e.g., Feature Used Multiple Times] | Repeat usage of a core feature | feature_name, usage_count |
| [e.g., Return Visit After Lapse] | User returns after 7+ days away] | days_since_last_visit |

### Referral

| Event | Trigger | Properties |
|-------|---------|------------|
| [e.g., Invite Sent] | User sends an invitation | channel |
| [e.g., Referral Signup Completed] | Referred user completes signup | referrer_id |

### Revenue

| Event | Trigger | Properties |
|-------|---------|------------|
| [e.g., Pricing Page Viewed] | User visits pricing | plan_viewed |
| [e.g., Trial Started] | User activates a trial | trial_type |
| [e.g., Subscription Purchased] | User completes checkout | plan, amount, billing_cycle |
| [e.g., Subscription Renewed] | Subscription auto-renews | plan, period |

---

## Reporting Cadence

| Cadence | Audience | Metrics Reviewed | Owner |
|---------|---------|-----------------|-------|
| Daily | Engineering team | [Fill in: e.g., error rates, deploy status] | [Name] |
| Weekly | Product team | [Fill in: e.g., activation rate, feature usage] | [Name] |
| Monthly | Leadership | [Fill in: e.g., NSM, revenue, churn] | [Name] |
| Quarterly | Board / investors | [Fill in: e.g., OKR progress, growth rate] | [Name] |

## Related

- [kpis-metrics.md](./kpis-metrics.md)
- [../../01_strategy/okrs/okrs.md](../../01_strategy/okrs/okrs.md)
- [../../04_delivery/agile-process/sprint-planning.md](../../04_delivery/agile-process/sprint-planning.md)
