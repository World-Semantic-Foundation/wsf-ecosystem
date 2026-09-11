# Orchestrator (Keystone)

> **The central entity that provides the core platform, sets standards, and manages ecosystem health.**

```yaml
semantic_id: wsf:Orchestrator
preferred_name: Orchestrator
aliases: [Focal Firm, Keystone]
status: Baseline
version: 0.1.0
classification: Tier 3 (Specialisation)
parent: wsf:Actor
domain: Business Ecosystem
```

## Definition

**Short:** The central entity that provides the core platform, sets standards, manages ecosystem health, and shapes the rules of engagement — creating shared value rather than merely extracting it.

**Intuition:** The "lead animal" of the ecosystem — not always the largest, but the one whose decisions most shape the system's behaviour.

## Necessary conditions

1. All Actor necessary conditions (inherited).
2. **Platform provision** — MUST provide (or orchestrate) a core Platform.
3. **Standards setting** — MUST set or enforce ecosystem standards (technical, contractual, or normative).
4. **Ecosystem health management** — MUST engage in actions that affect ecosystem-level health.

## Constraints

- The keystone-to-dominator drift is a **governance failure mode**, not a different classification — a Keyston's drift into extraction transforms it into a `wsf:Dominator` (see `dominator.md`).

## Relationships

- **Specialises:** `wsf:Actor`
- **Specialised by:** `wsf:Dominator` (degraded variant)
- **Related to:** `wsf:Platform`, `wsf:Boundary Resources`, `wsf:Governance`, `wsf:Ecosystem Health`

## Canonical example

Apple Inc. as Orchestrator of the iOS ecosystem; OTCHERE Inc. as Orchestrator of the OTCHERE Commerce Ecosystem.

---

*Orchestrator is a Tier 3 specialisation of Actor. Status: Baseline.*
