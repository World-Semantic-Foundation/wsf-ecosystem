# Complementor (Niche Player)

> **An entity that creates value by adding specialised products, services, or content to the core platform.**

```yaml
semantic_id: wsf:Complementor
preferred_name: Complementor
aliases: [Niche Player]
status: Baseline
version: 0.1.0
classification: Tier 3 (Specialisation)
parent: wsf:Actor
domain: Business Ecosystem
```

## Definition

**Short:** An actor that creates value by adding specialised products, services, or content to the core platform, increasing its overall utility.

**Intuition:** The actors that "complete" the platform by filling niches the Orchestrator does not serve — third-party app developers, integrators, content creators, downstream service providers.

## Necessary conditions

1. All Actor necessary conditions (inherited).
2. **Platform complementarity** — MUST create offerings that increase the platform's value to other actors.
3. **Independence of offering** — MUST produce offerings not already provided by the Orchestrator (otherwise it is redundant, not complementary).

## Constraints

- Complementors depend on the platform yet may compete with the Orchestrator (coopetition) — see `research/03-relationship-grammar/` Rule R2.
- Survival rate of complementors is a key indicator of Ecosystem Health (specifically `Niche Creation`).

## Relationships

- **Specialises:** `wsf:Actor`
- **Related to:** `wsf:Orchestrator`, `wsf:Boundary Resources`, `wsf:Network Effect (Indirect)`, `wsf:Coopetition`

## Canonical example

Third-party iOS app developers; OTCHERE Marketplace sellers; AWS consulting partners.

---

*Complementor is a Tier 3 specialisation of Actor. Status: Baseline.*
