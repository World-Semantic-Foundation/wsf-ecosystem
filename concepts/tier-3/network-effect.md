# Network Effect

> **The phenomenon where a product or service gains additional value as more actors use it — an emergent property of actor relationships.**

```yaml
semantic_id: wsf:Network Effect
preferred_name: Network Effect
aliases: [NE]
status: Baseline
version: 0.1.0
classification: Tier 3 (Specialisation — disposition)
parent: wsf:Disposition
domain: Value Dynamics
subtypes: [wsf:Direct Network Effect, wsf:Indirect Network Effect]
```

## Definition

**Short:** The phenomenon where a product or service gains additional value as more actors use it — modelled as an emergent property of the relationships between actor classes.

**Intuition:** The more people use it, the more valuable it gets. The key insight from network economics.

## Necessary conditions

1. All Disposition necessary conditions (inherited).
2. **Multi-actor dependency** — value MUST depend on the number of actors participating.
3. **Relational grounding** — MUST be a property of the actor network (the platform + its users + its complementors), not of any single actor.

## Constraints

- Network effects can be negative (congestion, dilution).
- Cross-side effects require balancing both sides — a classic cold-start problem.

## Relationships

- **Specialises:** `wsf:Disposition`
- **Specialised by:** `wsf:Direct Network Effect`, `wsf:Indirect Network Effect`
- **Related to:** `wsf:Lock-In` (production), `wsf:Switching Costs` (cause), `wsf:Marketplace` (primary substrate)

---

*Network Effect is a Tier 3 specialisation of Disposition. Status: Baseline.*
