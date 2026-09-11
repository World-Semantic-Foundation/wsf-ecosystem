# Lifecycle Stages

> **The four temporal states an ecosystem moves through, per James F. Moore's lifecycle model.**

```yaml
collection_semantic_id: wsf:Ecosystem Lifecycle Stages
classification: Tier 3 (Specialisation — states)
parent: wsf:State
domain: Temporal
stages: [Birth, Expansion, Leadership, Self-Renewal or Death]
```

## Overview

An ecosystem MUST be modelled with temporal state — health metrics, governance needs, and dominant risks differ per stage.

## The four stages

### Birth (Define Value Proposition)
**Definition:** The phase of establishing the core value and attracting early adopters.
**Concerns:** Cold-start problem; crisp value proposition required; trajectory-setting governance.

### Expansion (Supply & Demand Scaling)
**Definition:** The phase focused on scaling network effects and onboarding complementors.
**Concerns:** Quality dilution; infrastructure bottlenecks; premature monetisation.

### Leadership / Authority
**Definition:** The mature phase of maintaining stability, managing coopetition, and defending against disruptors.
**Concerns:** Dominator drift; bureaucratic ossification; lock-in complacency.

### Self-Renewal or Death
**Definition:** The critical bifurcation: radically innovate to survive external shocks, or decline into obsolescence.
**Concerns:** The most consequential transition; Boundary Spanners and external sensing are decisive.

## Modelling rules

- Stages are **states**, not a strictly linear path. Allowed transitions:
  - Birth → Expansion → Leadership → Self-Renewal/Death (canonical)
  - Self-Renewal/Death → Birth (after successful renewal — regress to a new Birth state)
  - Leadership → Expansion (after major shock)
- Each stage MUST be asserted with time validity period.
- Health, governance, and risk profiles differ per stage — prescriptive analysis requires stage context.

## Per-stage concept files

- `concepts/lifecycle/birth.md`
- `concepts/lifecycle/expansion.md`
- `concepts/lifecycle/leadership.md`
- `concepts/lifecycle/self-renewal-or-death.md`

---

*Lifecycle Stages is a curated collection of Tier 3 state specialisations. Status: Baseline.*
