# Modularity

> **The architectural property allowing the ecosystem to be decomposed into independent, interchangeable components.**

```yaml
semantic_id: wsf:Modularity
preferred_name: Modularity
status: Baseline
version: 0.1.0
classification: Tier 3 (Specialisation — disposition)
parent: wsf:Disposition
domain: Structure
```

## Definition

**Short:** The architectural property allowing the ecosystem to be decomposed into independent, interchangeable components with defined interfaces.

**Intuition:** What enables parallel innovation by complementors without forcing them to coordinate.

## Necessary conditions

1. All Disposition necessary conditions (inherited — modularity is a disposition of the platform).
2. **Decomposability** — The system MUST be decomposable into independently-modifiable components.
3. **Interface definition** — Component interfaces MUST be specified and stable.

## Constraints

- High modularity reduces coupling but can fragment standards.
- Hidden dependencies (shared data models) undermine nominal modularity.

## Relationships

- **Specialises:** `wsf:Disposition`
- **Related to:** `wsf:Coupling Level`, `wsf:Interoperability Standards`, `wsf:Boundary Resources`

---

*Modularity is a Tier 3 specialisation of Disposition. Status: Baseline.*
