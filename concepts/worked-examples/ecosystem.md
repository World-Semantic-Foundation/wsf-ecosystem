# Ecosystem

> **A complex, adaptive system composed of multiple interacting Entities that exchange Value, share a Context, exhibit mutual influence, and produce emergent, system-level properties.**

## Semantic Identity

```yaml
semantic_id: wsf:Ecosystem
preferred_name: Ecosystem
aliases: [Ecosystem (general), System-of-Systems]
status: Baseline (worked-example designation pending ADR-WSF-28 ratification)
version: 0.1.0
defined_by: ADR-WSF-28 (proposed)
classification: Tier 3 (Worked Example: analogous to Capability)
parent: wsf:System
domain: Condition (Emergent properties)
```

## Definition

**Short:** A system of interacting entities exhibiting emergent properties through mutual influence within a shared context.

**Long:** An Ecosystem is a complex, adaptive system composed of multiple interacting Entities (organisations, individuals, or digital agents) that exchange Value, share a Context, exhibit mutual influence, and produce emergent, system-level properties that none of the constituent entities produces alone. An Ecosystem is bounded by the set of entities whose behaviour materially affects and is affected by the other entities within the system.

**Intent:** To provide the foundational domain primitive for ecosystem ontology: a concept that can ground the entire ecosystem vocabulary (actors, platforms, value dynamics, governance, lifecycle, health) without requiring the foundation to absorb every domain construct.

**Intuition:** What you have when the relationships *between* entities become as consequential as the entities *themselves*: when the whole genuinely exhibits behaviours no part exhibits alone.

## Conditions

### Necessary conditions

1. **Multiplicity of entities**: MUST involve more than one Entity.
2. **Interaction**: Entities MUST interact (Value Exchange, Assertion, or other Relationship kinds).
3. **Mutual influence**: Behaviour of each entity MUST materially affect and be affected by others.
4. **Shared context**: All entities MUST operate within a Context.
5. **Emergence**: The system MUST exhibit properties (Network Effects, Lock-In, Health, Lifecycle) not attributable to any single entity.

### Sufficient conditions

A set of entities is an Ecosystem iff it satisfies all five necessary conditions AND the relations among entities carry WSF relational content (not merely structural edges).

## Constraints

- **Inclusion:** MUST involve distinguishable entities with identity; MUST have interaction patterns assertable.
- **Exclusion:** MUST NOT be a synonym for `System` (an Ecosystem is a *kind* of System); MUST NOT be a synonym for `Market` or `Industry`.
- **Boundary:** Distinguished from `System` by (a) agency of components, (b) mutual-influence requirement, (c) expectation of emergence.

## Relationships

- **Specialises:** `wsf:System`
- **Specialised by:** `wsf:Business Ecosystem`, `wsf:Digital Business Ecosystem`, `wsf:Economic Ecosystem`, `wsf:Innovation Ecosystem`
- **Related to:** `wsf:Entity` (members), `wsf:Relationship` (interactions), `wsf:Context` (shared context), `wsf:Disposition` (Network Effects, Health, Lock-In)

## Examples

### Positive

- A mobile platform with developers, users, advertisers, and device manufacturers.
- A healthcare ecosystem with providers, payers, patients, regulators, and pharmaceutical companies.
- An open-source software ecosystem with maintainers, contributors, packagers, and end users.

### Negative

- A single company with internal departments.
- A market segment (analytical lens, not a system of agents).
- A static list of companies in the same industry.

### Borderline

- A consortium with shared legal vehicle but minimal operational interaction (qualifies if interactions exceed mere co-membership).
- A supply chain with one-directional flow (qualifies if feedback loops create mutual influence).

## Context applicability

- **Universal:** false
- **Applicable contexts:** business strategy, platform economics, innovation studies, ecological biology (borrowed term), digital transformation

## Governance

- **Authority:** WSF
- **ADR:** ADR-WSF-28 (proposed)
- **History:** Initial draft, v0.1.0

## Provenance

- **Source:** Moore (1993); Iansiti & Levien (2004); Gawer & Cusumano (2002, 2014); Rochet & Tirole (2003); Guarino & Welty (2009)
- **Asserted by:** WSF Ecosystem Working Group
- **Evidence:** Cross-discipline convergence; demonstrated utility in strategy and engineering; consistent with WSF Tier 1 primitives
- **References:** VOCAB-000 v2.0 §2.1; ADR-CONCEPTS-01.md §1

## Canonical example (per WSF Example Consistency Principle)

```yaml
ecosystem:
  semantic_id: wsf-ex:OTCHERE-Platform-Ecosystem
  preferred_name: OTCHERE Platform Ecosystem
  classification: Worked Example
  parent: wsf:Ecosystem
  members:
    - entity: wsf-ex:OTCHERE-Inc
      role: Orchestrator
    - entity: wsf-ex:Complementor-A
      role: Complementor
    - entity: wsf-ex:Complementor-B
      role: Complementor
    - entity: wsf-ex:Gatekeeper-Service
      role: Gatekeeper
    - entity: wsf-ex:User-Population
      role: User / Prosumer (overlapping)
  shared_context:
    domain: Enterprise commerce
    period: 2024-01-01 to present
  emergent_properties:
    - wsf:Network Effect (Indirect / Cross-Side)
    - wsf:Lock-In (emerging)
    - wsf:Ecosystem Health (mature)
  lifecycle_stage: wsf:Expansion
  measured_by:
    - wsf:Productivity
    - wsf:Robustness
    - wsf:Niche Creation
```

## Cross-references

- ADR-WSF-17 (Foundational Semantic Architecture): defines the Tier 3 specialisation pattern
- ADR-WSF-04 (Semantic Inheritance): governs specialisation rules
- ADR-WSF-20 (Concept Definition Model): defines this concept's metadata schema
- ADR-WSF-07 (Capacity, Ability, and Capability): precedent for worked-example treatment

---

*Ecosystem is a Tier 3 worked example grounded in System (Tier 1). Status: Baseline (pending ADR-WSF-28 ratification).*
