# Digital Business Ecosystem

> **A Business Ecosystem where digital technology is the primary medium of value interaction and exchange.**

## Semantic Identity

```yaml
semantic_id: wsf:Digital Business Ecosystem
preferred_name: Digital Business Ecosystem
aliases: [DBE]
status: Baseline
version: 0.1.0
defined_by: ADR-WSF-28 (proposed)
classification: Tier 3 (Specialisation)
parent: wsf:Business Ecosystem
domain: Digital Transformation / Platform Strategy
```

## Definition

**Short:** A Business Ecosystem in which digital technology (software platforms, data infrastructure, APIs, digital services, or digital artefacts) constitutes the primary medium of interaction, value exchange, and co-creation.

**Intent:** To specialise Business Ecosystem with the digital-medium constraint: the most commercially consequential subtype in the current era.

**Intuition:** What you have when interactions between business actors are mediated by digital artefacts (APIs, software platforms, data flows) to such a degree that the digital substrate is the dominant enabler.

## Conditions

### Necessary

1. All Business Ecosystem necessary conditions (inherited).
2. **Digital-medium constraint**: a significant majority of interactions, exchanges, and assertions MUST be mediated by digital artefacts.
3. **Digital artefact agency**: software, data, or algorithmic systems MUST play a non-trivial role.

### Sufficient

A Business Ecosystem is a Digital Business Ecosystem iff it satisfies all Business Ecosystem conditions AND digital artefacts constitute the primary medium of value-exchange relationships AND the digital substrate is materially constitutive of emergent properties.

## Constraints

- **Inclusion:** MUST involve at least one Platform with digital interfaces; MUST exhibit data-driven value flows.
- **Exclusion:** MUST NOT be an analog business ecosystem.
- **Boundary:** Distinguished from Business Ecosystem by digital-medium constraint; from Platform (which is the asset, not the ecosystem of users + complementors).

## Relationships

- **Specialises:** `wsf:Business Ecosystem`
- **Specialised by:** `wsf:Platform Ecosystem`, `wsf:API Ecosystem`, `wsf:Data Ecosystem`, `wsf:Marketplace Ecosystem`
- **Related to:** `wsf:Platform`, `wsf:Boundary Resources`, `wsf:Interoperability Standards`, `wsf:Prosumer`, `wsf:Gatekeeper`

## Examples

- **Positive:** AWS partner ecosystem; OTCHERE Marketplace; Stripe API ecosystem.
- **Negative:** Traditional physical-goods wholesale ecosystem without significant digital mediation.
- **Borderline:** Click-and-mortar retail with significant but not dominant digital mediation.

## Canonical example

```yaml
digital_business_ecosystem:
  semantic_id: wsf-dbe:OTCHERE-Marketplace-Ecosystem
  preferred_name: OTCHERE Marketplace Digital Business Ecosystem
  parent: wsf:Business Ecosystem
  digital_medium:
    platform: wsf-plat:OTCHERE-Marketplace
    boundary_resources:
      - wsf-br:Seller-API
      - wsf-br:Buyer-Web-Surface
      - wsf-br:Mobile-SDK
    interoperability_standards: [REST, OAuth 2.0, OTCHERE Product Schema]
    gatekeeping: Algorithmic + human curation
  members:
    - entity: wsf-ex:OTCHERE-Inc
      role: Orchestrator
    - entity: wsf-ex:Seller-A
      role: Complementor
    - entity: wsf-ex:Algorithmic-Curator
      role: Gatekeeper (automated)
  lifecycle_stage: wsf:Leadership
```

---

*Digital Business Ecosystem is a Tier 3 specialisation of Business Ecosystem. Status: Baseline.*
