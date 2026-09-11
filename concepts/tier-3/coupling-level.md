# Coupling Level

> **A descriptive structural property defining the degree of dependency between actors.**

```yaml
semantic_id: wsf:Coupling Level
preferred_name: Coupling Level
aliases: [Coupling Degree, Tightness]
status: Baseline
version: 0.1.0
classification: Tier 3 (Specialisation — descriptive property)
parent: wsf:Relationship
domain: Structure
```

## Definition

**Short:** A descriptive structural property defining the degree of dependency between actors: tightly coupled (deep integration, high dependency) vs. loosely coupled (independent, standardised interaction).

**Intuition:** A property of actor-actor (or actor-platform) relationships, not of actors themselves.

## Necessary conditions

1. All Relationship necessary conditions (inherited).
2. **Degree assertion** — MUST specify the degree (Tight or Loose) and the dimension (technical, contractual, data, etc.).
3. **Pairwise scoping** — MUST be asserted per actor pair, not globally.

## Constraints

- Neither extreme is universally good — tight coupling enables deep value creation; loose coupling enables resilience.

## Relationships

- **Specialises:** `wsf:Relationship`
- **Related to:** `wsf:Modularity`, `wsf:Robustness`, `wsf:Value Exchange`

---

*Coupling Level is a Tier 3 specialisation of Relationship. Status: Baseline.*
