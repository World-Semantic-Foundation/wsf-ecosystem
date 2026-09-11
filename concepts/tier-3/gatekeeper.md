# Gatekeeper / Curator

> **The entity responsible for quality control, security, and standards enforcement.**

```yaml
semantic_id: wsf:Gatekeeper
preferred_name: Gatekeeper
aliases: [Curator, Quality Controller]
status: Baseline
version: 0.1.0
classification: Tier 3 (Specialisation)
parent: wsf:Actor
domain: Governance
```

## Definition

**Short:** The actor (or automated system) responsible for quality control, security, and standards enforcement before a complementor's offering reaches the end-user.

**Intuition:** The bouncer at the door of the ecosystem: sets and enforces the quality bar that determines which offerings are admitted.

## Necessary conditions

1. All Actor necessary conditions (inherited).
2. **Standards authority**: MUST have authority to admit, reject, or remove offerings.
3. **Quality enforcement**: MUST apply quality, security, or compliance criteria.

## Constraints

- Gatekeeping trades safety/trust against innovation speed and openness.
- Algorithmic gatekeeping introduces opacity and bias risks.

## Relationships

- **Specialises:** `wsf:Actor`
- **Related to:** `wsf:Governance`, `wsf:Trust Mechanisms`, `wsf:Interoperability Standards`, `wsf:Orchestrator` (typically delegated by)

---

*Gatekeeper is a Tier 3 specialisation of Actor. Status: Baseline.*
