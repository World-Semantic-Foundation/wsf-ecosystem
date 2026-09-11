# Coopetition

> **A state in which actors simultaneously cooperate (to grow the total market) and compete (to capture a larger share of the resulting value).**

```yaml
semantic_id: wsf:Coopetition
preferred_name: Coopetition
status: Baseline
version: 0.1.0
classification: Tier 3 (Specialisation — state + relational pattern)
parent: wsf:State
domain: Governance / Value Dynamics
```

## Definition

**Short:** The co-existence state of cooperative AND competitive relationships between the same actor pair at different layers — modelled as a State plus a relational pattern (`cooperates_with` ∧ `competes_with`, scoped per layer).

**Intuition:** The defining dynamic of mature ecosystems — Apple cooperates with developers on the App Store AND competes with them in services.

## Constraints

- Hardest concept to model formally — requires context-scoping per layer.
- Per Rule R2 in `research/03-relationship-grammar/`: coopetition is the co-existence of the two predicates with non-overlapping layer contexts.

## Relationships

- **Specialises:** `wsf:State`
- **Related to:** `wsf:Complementor`, `wsf:Orchestrator`, `wsf:Value Slippage`, `wsf:Decision Rights Allocation`

---

*Coopetition is a Tier 3 specialisation of State. Status: Baseline.*
