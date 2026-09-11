# Proposal 01: Ecosystem as a Tier 3 Worked Example (Specialisation of `wsf:System`)

> **Status:** Candidate → Investigating
> **Proposed tier:** Worked Example (Tier 3 + demonstration status, analogous to `Capability`)
> **Proposed parent:** `wsf:System`
> **Proposed ADR:** ADR-WSF-28 (subject to numbering reconciliation)
> **Authoring rationale:** Per Principle 2 (Minimal Foundation), `Ecosystem` fails the irreducibility test for Tier 1. Per Principle 3 (Explicit Specialization), it must be a specialisation of an existing Tier 1 primitive. Per the precedent set by `Capability`, the most consequential Tier 3 specialisation in a domain merits worked-example status with full ADR-WSF-20 §14 treatment.

---

## 1. Definition (long)

An **Ecosystem** is a complex, adaptive system composed of multiple interacting Entities (organisations, individuals, or digital agents) that exchange Value, share a Context, exhibit mutual influence, and produce emergent, system-level properties that none of the constituent entities produces alone. An Ecosystem is bounded by the set of entities whose behaviour materially affects and is affected by the other entities within the system.

## 2. Definition (short)

A system of interacting entities exhibiting emergent properties through mutual influence within a shared context.

## 3. Intent

To provide the foundational domain primitive for ecosystem ontology: a concept that can ground the entire ecosystem vocabulary (actors, platforms, value dynamics, governance, lifecycle, health) without requiring the foundation to absorb every domain construct.

## 4. Intuition

An ecosystem is what you have when the relationships *between* entities become as consequential as the entities *themselves*: when the whole genuinely exhibits behaviours no part exhibits alone (Moore's "co-evolution", Iansiti & Levien's "keystone advantage", network effects, lock-in).

## 5. Necessary conditions

1. **Multiplicity of entities.** MUST involve more than one Entity. A single entity is not an ecosystem.
2. **Interaction.** Entities MUST interact: through Value Exchange, Assertion, or other Relationship kinds: not merely coexist.
3. **Mutual influence.** The behaviour of each entity MUST materially affect and be affected by the others.
4. **Shared context.** All entities MUST operate within a Context (organisational, technological, regulatory, geographic, or market).
5. **Emergence.** The system as a whole MUST exhibit properties (Network Effects, Lock-In, Health, Lifecycle stage) that are not attributable to any single entity.

## 6. Sufficient conditions

A set of entities is an Ecosystem if and only if:

- it satisfies all five necessary conditions, AND
- the relations among entities can be characterised using WSF relational properties from `wsf-rel:*` (i.e., the entity interactions carry semantic content, not merely structural edges).

## 7. Constraints

- **Inclusion:** MUST involve distinguishable entities with identity, MUST have interaction patterns that can be asserted.
- **Exclusion:** MUST NOT be a synonym for `System` (an Ecosystem is a *kind* of System, not equivalent); MUST NOT be a synonym for `Market` or `Industry` (these are analytical lenses, not system-level entities with agency); MUST NOT collapse into a single Organisation.
- **Boundary:** Distinguished from `System` by (a) the agency of its components, (b) the requirement of mutual influence, and (c) the expectation of emergence.

## 8. Relationships

- **Specialises:** `wsf:System`
- **Specialised by:** `wsf:Business Ecosystem`, `wsf:Digital Business Ecosystem`, `wsf:Economic Ecosystem`, `wsf:Innovation Ecosystem`, …
- **Related to:** `wsf:Entity` (members are entities), `wsf:Relationship` (interactions are relationships), `wsf:Context` (shared context), `wsf:Disposition` (Network Effects, Health, Lock-In are dispositions of the ecosystem-as-system).

## 9. Examples

### Positive

- A mobile platform with developers, users, advertisers, and device manufacturers: mutual influence via Network Effects and shared context of the platform.
- A healthcare ecosystem with providers, payers, patients, regulators, and pharmaceutical companies: shared context of the regulatory and clinical environment.
- An open-source software ecosystem with maintainers, contributors, downstream packagers, and end users: shared context of the code repository and governance rules.

### Negative

- A single company with internal departments (no multi-entity interaction in the ecosystem sense).
- A market segment (analytical lens, not a system of interacting agents).
- A static list of companies in the same industry (no asserted mutual influence required).

### Borderline

- A consortium of firms with a shared legal vehicle but minimal operational interaction (qualifies if interactions exceed mere co-membership).
- A supply chain with sequential, one-directional value flow (qualifies if feedback loops create mutual influence).

## 10. Context applicability

- **Universal:** false: Ecosystem is a domain-level concept, not a universal primitive.
- **Applicable contexts:** business strategy, platform economics, innovation studies, ecological biology (borrowed term), digital transformation.

## 11. Governance

- **Authority:** WSF
- **ADR:** This proposal (ADR-WSF-28 candidate)
- **History:** Initial draft, version 0.1.0

## 12. Provenance

- **Source:** Strategy literature (Moore 1993; Iansiti & Levien 2004; Gawer & Cusumano 2002, 2014); platform economics (Rochet & Tirole 2003); ontology engineering practice (Guarino & Welty 2009).
- **Asserted by:** WSF Ecosystem Working Group
- **Evidence:** Cross-discipline convergence on the construct; demonstrated utility in strategy and engineering; consistent with WSF Tier 1 primitives.
- **References:** See VOCAB-000 v2.0 references.

## 13. Worked-example designation rationale

Per ADR-WSF-17 §"Disposition Model" and the precedent of `Capability`, a domain construct of sufficient explanatory power merits worked-example treatment. `Ecosystem` qualifies because:

- It is the **root concept** of an entire domain (business ecosystem, digital ecosystem, innovation ecosystem, etc.).
- It grounds a **relational layer** that other WSF concepts do not need (the "verbs" of ecosystem ontology).
- Its worked-example treatment **demonstrates the full specialisation chain**: Tier 1 primitive (`wsf:System`) → Tier 3 specialisation (`Ecosystem`) → Tier 3 sub-specialisations (`Business Ecosystem`, `Digital Business Ecosystem`) → actor taxonomy and value dynamics.

## 14. Canonical example (per WSF Example Consistency Principle)

```yaml
ecosystem:
  semantic_id: wsf-ex:OTCHERE-Platform-Ecosystem
  preferred_name: OTCHERE Platform Ecosystem
  status: Baseline
  classification: Worked Example (Tier 3)
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

## 15. Next steps

1. File this proposal as `INV-FIND-WSF-28-Ecosystem.md` and reconcile against existing ADR sequence.
2. Raise ADR-WSF-28 (or the next free number) proposing `Ecosystem` as a Tier 3 worked example of `wsf:System`.
3. Author dependent concept files (`business-ecosystem.md`, `digital-business-ecosystem.md`).
4. Author the relational properties file (the "verbs").
5. File a CR for the implementation in `wsf-spec/`.

---
*This proposal establishes `Ecosystem` as a Tier 3 worked example within WSF. Implementation proceeds through subsequent ADRs and CRs.*
