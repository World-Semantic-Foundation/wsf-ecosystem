# Boundary Resources

> **The tools, interfaces, and documentation provided by the Orchestrator to enable Complementors to build on the platform.**

```yaml
semantic_id: wsf:Boundary Resources
preferred_name: Boundary Resources
aliases: [BRs]
status: Baseline
version: 0.1.0
classification: Tier 3 (Specialisation)
parent: wsf:Entity
domain: Structure (Gawer's construct)
```

## Definition

**Short:** The tools, interfaces, and documentation provided by the Orchestrator to enable Complementors to build on the platform — e.g., APIs, SDKs, sandboxes, developer portals (Gawer).

**Intuition:** The "open door" of the platform — concrete, engineered surfaces that determine what complementors can build.

## Necessary conditions

1. All Entity necessary conditions (inherited).
2. **Orchestrator provision** — MUST be provided by an Orchestrator (or a delegated actor).
3. **Complementor enabling** — MUST be designed for and consumable by Complementors.

## Constraints

- Design is strategic: too open invites value slippage and dominator risk; too closed prevents complementor investment. Boundary Resources encode governance technically.
- Measurement of openness and effectiveness is a `Boundary Spanner` and `Orchestrator` responsibility.

## Relationships

- **Specialises:** `wsf:Entity`
- **Related to:** `wsf:Orchestrator`, `wsf:Complementor`, `wsf:Governance`, `wsf:Modularity`, `wsf:Interoperability Standards`

---

*Boundary Resources is a Tier 3 specialisation of Entity (Gawer construct). Status: Baseline.*
