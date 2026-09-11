# Business Ecosystem

> **A value-oriented ecosystem of organisations and economic actors operating within a shared market and regulatory context.**

## Semantic Identity

```yaml
semantic_id: wsf:Business Ecosystem
preferred_name: Business Ecosystem
aliases: [BEcosys]
status: Baseline
version: 0.1.0
defined_by: ADR-WSF-28 (proposed)
classification: Tier 3 (Specialisation)
parent: wsf:Ecosystem
domain: Business Strategy / Platform Economics
```

## Definition

**Short:** A Business Ecosystem is an Ecosystem whose constituent entities are primarily organisations, individuals, or economic actors; whose interactions are oriented toward the creation, exchange, and capture of economic value; and whose shared context is shaped by market, regulatory, and competitive forces.

**Intent:** To specialise the general Ecosystem concept with the domain constraints that define business ecosystems.

**Intuition:** What you have when companies, customers, suppliers, complementors, and regulators form a recognisable community whose behaviour shapes and is shaped by market dynamics.

## Conditions

### Necessary

1. All Ecosystem necessary conditions (inherited).
2. **Economic agency** — constituent entities MUST have economic agency.
3. **Value orientation** — interactions MUST be oriented toward value creation, exchange, or capture.
4. **Shared market context** — entities MUST operate within a shared market, regulatory, or competitive context.

### Sufficient

An Ecosystem is a Business Ecosystem iff all five Ecosystem necessary conditions hold AND at least one constituent entity exhibits value-creation behaviour AND the shared context includes a market, regulatory, or competitive dimension.

## Constraints

- **Inclusion:** MUST contain at least one Orchestrator or analogous central actor; MUST exhibit some form of Value Co-creation.
- **Exclusion:** MUST NOT be a pure technology ecosystem; MUST NOT be a biological ecosystem (out of scope).
- **Boundary:** Distinguished from generic Ecosystem by economic agency; from Digital Business Ecosystem by absence of digital-medium constraint.

## Relationships

- **Specialises:** `wsf:Ecosystem`
- **Specialised by:** `wsf:Digital Business Ecosystem`, `wsf:Innovation Ecosystem`, `wsf:Service Ecosystem`
- **Related to:** `wsf:Organisation` (Orchestrator), `wsf:Capability`, `wsf:Market`, `wsf:Policy`

## Examples

- **Positive:** Apple iOS ecosystem; OTCHERE Commerce Ecosystem; healthcare ecosystem with providers, payers, patients, regulators.
- **Negative:** Open-source community without economic value exchange; pure consumer social network without business actors.
- **Borderline:** Non-profit consortium with significant funding flows; government services ecosystem with economic actors.

## Canonical example

```yaml
business_ecosystem:
  semantic_id: wsf-becosys:OTCHERE-Commerce-Ecosystem
  preferred_name: OTCHERE Commerce Ecosystem
  parent: wsf:Ecosystem
  members:
    - entity: wsf-ex:OTCHERE-Inc
      role: Orchestrator
    - entity: wsf-ex:Complementor-Partner-1
      role: Complementor
    - entity: wsf-ex:EndCustomer-Enterprise-A
      role: Consumer / Prosumer (overlapping)
    - entity: wsf-ex:RegulatoryAuthority
      role: External Authority (Boundary Spanner target)
  value_orientation: B2B commerce enablement
  lifecycle_stage: wsf:Expansion
```

---

*Business Ecosystem is a Tier 3 specialisation of Ecosystem. Status: Baseline.*
