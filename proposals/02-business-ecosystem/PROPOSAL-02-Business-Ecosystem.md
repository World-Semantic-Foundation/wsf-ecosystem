# Proposal 02 — Business Ecosystem (Tier 3 Specialisation of `wsf:Ecosystem`)

> **Status:** Candidate → Investigating
> **Proposed tier:** Tier 3 (specialisation)
> **Proposed parent:** `wsf:Ecosystem`
> **Depends on:** Proposal 01 (`Ecosystem`) being ratified

---

## 1. Definition (long)

A **Business Ecosystem** is an Ecosystem whose constituent entities are primarily organisations, individuals, or economic actors; whose interactions are oriented toward the creation, exchange, and capture of economic value; and whose shared context is shaped by market, regulatory, and competitive forces. A Business Ecosystem is characterised by interdependence, co-evolution, non-linearity, decentralisation, and shared fate among its members.

## 2. Definition (short)

A value-oriented ecosystem of organisations and economic actors operating within a shared market and regulatory context.

## 3. Intent

To specialise the general Ecosystem concept with the domain constraints that define business ecosystems — distinguishing them from biological, technological-infrastructural, or purely digital ecosystems that lack the value-creation orientation.

## 4. Intuition

A business ecosystem is what you have when companies, customers, suppliers, complementors, and regulators form a recognisable community whose behaviour shapes and is shaped by market dynamics — Moore's "economic community" of "organisms and their environment".

## 5. Necessary conditions

1. **All Ecosystem necessary conditions** (inherited).
2. **Economic agency.** Constituent entities MUST have economic agency — they produce, exchange, or capture value.
3. **Value orientation.** Interactions MUST be oriented toward value creation, exchange, or capture (not purely informational or recreational).
4. **Shared market context.** Entities MUST operate within a shared market, regulatory, or competitive context.

## 6. Sufficient conditions

An Ecosystem is a Business Ecosystem if and only if:

- it satisfies all Ecosystem necessary conditions, AND
- at least one constituent entity exhibits value-creation behaviour (production, exchange, or capture), AND
- the shared context includes a market, regulatory, or competitive dimension.

## 7. Constraints

- **Inclusion:** MUST contain at least one Orchestrator or analogous central actor; MUST exhibit some form of Value Co-creation.
- **Exclusion:** MUST NOT be a pure technology ecosystem (use `Digital Ecosystem` if the substrate is the primary defining feature); MUST NOT be a biological ecosystem (out of WSF scope by domain).
- **Boundary:** Distinguished from generic `Ecosystem` by the economic agency constraint and value orientation; distinguished from `Digital Business Ecosystem` by the absence of a digital-medium constraint.

## 8. Relationships

- **Specialises:** `wsf:Ecosystem`
- **Specialised by:** `wsf:Digital Business Ecosystem`, `wsf:Innovation Ecosystem`, `wsf:Service Ecosystem`, …
- **Related to:** `wsf:Organisation` (typical Orchestrator), `wsf:Capability` (enabling construct), `wsf:Market` (boundary context), `wsf:Policy` (regulatory dimension).

## 9. Examples

### Positive

- The Apple iOS ecosystem (Apple as Orchestrator, developers as Complementors, users as Consumers/Prosumers).
- A healthcare ecosystem with providers, payers, patients, and regulators.
- The OTCHERE Inc platform ecosystem (OTCHERE Inc as Orchestrator, partner developers as Complementors, customer enterprises as Consumers).

### Negative

- An open-source community without economic value exchange (qualifies as Ecosystem but not Business Ecosystem).
- A pure consumer social network without business actors (qualifies as Ecosystem; may or may not qualify as Business Ecosystem depending on monetisation).

### Borderline

- A non-profit consortium with funding flows (qualifies if value exchange is economically significant).
- A government services ecosystem (qualifies if there are economic actors in the system).

## 10. Context applicability

- **Universal:** false
- **Applicable contexts:** business strategy, platform economics, enterprise architecture, public policy

## 11. Governance

- **Authority:** WSF
- **ADR:** This proposal
- **History:** Initial draft, v0.1.0

## 12. Provenance

- **Source:** Moore (1993); Iansiti & Levien (2004); VOCAB-000 v2.0 §2.2
- **Asserted by:** WSF Ecosystem Working Group
- **Evidence:** Foundational concept in business strategy and platform economics literature.

## 13. Canonical example

```yaml
business_ecosystem:
  semantic_id: wsf-becosys:OTCHERE-Commerce-Ecosystem
  preferred_name: OTCHERE Commerce Ecosystem
  status: Baseline
  classification: Tier 3 (Specialisation)
  parent: wsf:Ecosystem
  specialises: wsf:Ecosystem
  members:
    - entity: wsf-ex:OTCHERE-Inc
      role: Orchestrator (Keystone)
    - entity: wsf-ex:Complementor-Partner-1
      role: Complementor
    - entity: wsf-ex:Complementor-Partner-2
      role: Complementor
    - entity: wsf-ex:EndCustomer-Enterprise-A
      role: Consumer / Prosumer (overlapping)
    - entity: wsf-ex:RegulatoryAuthority
      role: External Authority (Boundary Spanner target)
  value_orientation: B2B commerce enablement
  shared_context:
    market: Enterprise commerce
    regulatory: GDPR / industry-specific
  emergent_properties:
    - wsf:Network Effect (Indirect / Cross-Side)
    - wsf:Coopetition (Orchestrator ↔ Complementor)
  lifecycle_stage: wsf:Expansion
```

## 14. Next steps

1. Once Proposal 01 is ratified, file this as a dependent CR.
2. Author `business-ecosystem.md` in `concepts/tier-3/` using the ADR-WSF-20 §14 schema.

---
*This proposal establishes `Business Ecosystem` as a Tier 3 specialisation of `Ecosystem` within WSF.*
