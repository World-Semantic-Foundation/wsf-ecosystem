# Proposal 03 — Digital Business Ecosystem (Tier 3 Specialisation of `wsf:Business Ecosystem`)

> **Status:** Candidate → Investigating
> **Proposed tier:** Tier 3 (specialisation)
> **Proposed parent:** `wsf:Business Ecosystem`
> **Depends on:** Proposals 01 and 02 being ratified

---

## 1. Definition (long)

A **Digital Business Ecosystem (DBE)** is a Business Ecosystem in which digital technology (software platforms, data infrastructure, APIs, digital services, or digital artefacts) constitutes the primary medium of interaction, value exchange, and co-creation among the constituent entities. In a DBE, the "species" include digital artefacts (software, services, data, algorithms) alongside the human and organisational actors that create and consume them.

## 2. Definition (short)

A Business Ecosystem where digital technology is the primary medium of value interaction and exchange.

## 3. Intent

To specialise the Business Ecosystem concept with the digital-medium constraint — distinguishing DBEs from ecosystems whose interactions are primarily physical, analog, or human-mediated. This is the most commercially consequential Business Ecosystem subtype in the current era.

## 4. Intuition

A digital business ecosystem is what you have when the interactions between business actors are mediated and constituted by digital artefacts — APIs, software platforms, data flows, digital services — to such a degree that the digital substrate is the dominant enabler and shaper of value creation.

## 5. Necessary conditions

1. **All Business Ecosystem necessary conditions** (inherited).
2. **Digital-medium constraint.** A significant majority of interactions, value exchanges, and assertions MUST be mediated by digital artefacts.
3. **Digital artefact agency.** Software, data, or algorithmic systems MUST play a non-trivial role in mediating interactions (gatekeeping, recommendation, automation, etc.).

## 6. Sufficient conditions

A Business Ecosystem is a Digital Business Ecosystem if and only if:

- it satisfies all Business Ecosystem necessary conditions, AND
- digital artefacts constitute the primary medium of at least the value-exchange relationships, AND
- the digital substrate is materially constitutive of the ecosystem's emergent properties (Network Effects, Lock-In, Health).

## 7. Constraints

- **Inclusion:** MUST involve at least one Platform with digital interfaces (APIs, SDKs, web/mobile surfaces); MUST exhibit data-driven value flows.
- **Exclusion:** MUST NOT be an analog business ecosystem (e.g., a traditional agricultural cooperative).
- **Boundary:** Distinguished from `Business Ecosystem` by the digital-medium constraint; distinguished from `Platform` (which is the asset, not the ecosystem of users + complementors + interactions).

## 8. Relationships

- **Specialises:** `wsf:Business Ecosystem`
- **Specialised by:** `wsf:Platform Ecosystem`, `wsf:API Ecosystem`, `wsf:Data Ecosystem`, `wsf:Marketplace Ecosystem`, …
- **Related to:** `wsf:Platform`, `wsf:Boundary Resources`, `wsf:Interoperability Standards`, `wsf:Prosumer`, `wsf:Gatekeeper`.

## 9. Examples

### Positive

- The AWS partner ecosystem (digital platform + developers + customers + data flows).
- A digital marketplace like OTCHERE Marketplace (platform + sellers + buyers + reviews + algorithmic curation).
- An API ecosystem like Stripe (platform + integrators + end applications + developers).

### Negative

- A traditional physical-goods wholesale ecosystem without significant digital mediation.
- A consulting services ecosystem where interactions are predominantly human-mediated.

### Borderline

- A "click-and-mortar" retail ecosystem with significant but not dominant digital mediation.
- A financial services ecosystem where core transactions are digital but relationship management is human-mediated.

## 10. Context applicability

- **Universal:** false
- **Applicable contexts:** platform strategy, digital transformation, fintech, e-commerce, SaaS, API economy

## 11. Governance

- **Authority:** WSF
- **ADR:** This proposal
- **History:** Initial draft, v0.1.0

## 12. Provenance

- **Source:** VOCAB-000 v2.0 §2.4; Digital Business Ecosystem research (Nachira 2002; DBE European research cluster); platform economics literature.
- **Asserted by:** WSF Ecosystem Working Group
- **Evidence:** Foundational concept in digital transformation and platform strategy.

## 13. Canonical example

```yaml
digital_business_ecosystem:
  semantic_id: wsf-dbe:OTCHERE-Marketplace-Ecosystem
  preferred_name: OTCHERE Marketplace Digital Business Ecosystem
  status: Baseline
  classification: Tier 3 (Specialisation)
  parent: wsf:Business Ecosystem
  specialises: wsf:Business Ecosystem
  digital_medium:
    platform: wsf-plat:OTCHERE-Marketplace
    boundary_resources:
      - wsf-br:Seller-API
      - wsf-br:Buyer-Web-Surface
      - wsf-br:Mobile-SDK
    interoperability_standards:
      - REST
      - OAuth 2.0
      - OTCHERE Product Schema
    gatekeeping: Algorithmic + human curation
  members:
    - entity: wsf-ex:OTCHERE-Inc
      role: Orchestrator
    - entity: wsf-ex:Seller-A
      role: Complementor
    - entity: wsf-ex:Seller-B
      role: Complementor
    - entity: wsf-ex:Buyer-C
      role: User / Prosumer (reviewer)
    - entity: wsf-ex:Algorithmic-Curator
      role: Gatekeeper (automated)
    - entity: wsf-ex:Reg-Affairs-Team
      role: Boundary Spanner
  value_orientation: Marketplace transaction intermediation
  emergent_properties:
    - wsf:Network Effect (Cross-Side, dominant)
    - wsf:Lock-In (via review history + integration)
    - wsf:Ecosystem Health (Productivity high, Niche Creation moderate)
  lifecycle_stage: wsf:Leadership
```

## 14. Next steps

1. Once Proposals 01 and 02 are ratified, file this as a dependent CR.
2. Author `digital-business-ecosystem.md` in `concepts/tier-3/` using the ADR-WSF-20 §14 schema.

---
*This proposal establishes `Digital Business Ecosystem` as a Tier 3 specialisation of `Business Ecosystem` within WSF.*
