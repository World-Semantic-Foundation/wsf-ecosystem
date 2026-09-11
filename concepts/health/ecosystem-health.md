# Ecosystem Health

> **The composite disposition of an ecosystem to sustain itself, measured through Productivity, Robustness, and Niche Creation.**

```yaml
semantic_id: wsf:Ecosystem Health
preferred_name: Ecosystem Health
status: Baseline
version: 0.1.0
classification: Tier 3 (Specialisation — parent disposition)
parent: wsf:Disposition
metrics: [wsf:Productivity, wsf:Robustness, wsf:Niche Creation]
```

## Definition

**Short:** The composite disposition of an ecosystem to sustain itself, decomposed into three Iansiti–Levien metrics.

## Axiomatic Positioning

Health is the composite outcome of Governance, Co-evolution, and Value Co-creation. The three metrics MUST be tracked together — a dominator ecosystem can score high on Productivity while dying on Niche Creation.

## Metric decomposition

| Metric | Definition | Concern |
|---|---|---|
| **Productivity** | Ability to turn inputs into outputs efficiently | For whom? Aggregate can mask orchestrator-only capture. |
| **Robustness** | Ability to survive shocks and actor failures | Correlates negatively with tight coupling. |
| **Niche Creation** | Ability to continuously create new businesses | The most forward-looking metric; first casualty of dominator behaviour. |

## Canonical example (OTCHERE Marketplace)

```yaml
health_assessment:
  ecosystem: wsf-dbe:OTCHERE-Marketplace-Ecosystem
  measured_at: 2026-Q3
  productivity: 0.82 # high — efficient marketplace operations
  robustness: 0.61 # moderate — tight coupling to OTCHERE Inc creates single-point-of-failure risk
  niche_creation: 0.43 # declining — signs of dominator drift via fee increases
  overall_health: 0.62 # moderate — productivity sustained, niche creation eroding
  recommendation: "Renew — address niche creation through complementor enablement before leadership erodes."
```

---

*Ecosystem Health is a Tier 3 specialisation of Disposition. Status: Baseline.*
