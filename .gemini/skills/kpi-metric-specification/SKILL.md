---
name: kpi-metric-specification
description: Defines KPIs and product metrics with clear formulas, segments, and instrumentation notes. Use when choosing north-star metrics, building metric trees, or aligning dashboards with strategy.
---

# KPI and metric specification

## When to use

- Defining or revising KPIs, guardrails, and segment cuts.
- Preventing ambiguous “engagement” or vanity metrics without definitions.

## Steps

1. Start from [`03_analysis/kpis-metrics/_overview.md`](../../../.productmap/03_analysis/kpis-metrics/_overview.md) and [`metrics-tracking.md`](../../../.productmap/03_analysis/kpis-metrics/metrics-tracking.md).
2. For each metric: definition, formula, unit, time window, segment dimensions, data source, and owner.
3. Relate metrics to goals/OKRs and flag leading vs lagging indicators.

## Delegation

Use [subagent-prompt.md](subagent-prompt.md) for a sub-agent that produces metric specs and trees.
