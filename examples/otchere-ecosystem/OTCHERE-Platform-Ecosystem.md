# OTCHERE Platform Ecosystem: Worked Example

> **The OTCHERE Platform Ecosystem**: the worked example demonstrating the full ecosystem domain ontology in action, using the canonical `OTCHERE Inc` enterprise and individual `Kwesi` per the WSF Example Consistency Principle.

## Ecosystem profile

```yaml
ecosystem:
  semantic_id: wsf-ex:OTCHERE-Platform-Ecosystem
  preferred_name: OTCHERE Platform Ecosystem
  classification: Tier 3 (Worked Example)
  parent: wsf:Ecosystem
  status: Baseline
  defined_by: ADR-WSF-28 (proposed)

  members:
    - entity: wsf-ex:OTCHERE-Inc
      role: Orchestrator (Keystone)
      context: OTCHERE Marketplace platform
      layer: Platform governance
    - entity: wsf-ex:Complementor-Seller-A
      role: Complementor
      context: OTCHERE Marketplace
      layer: Supply side
    - entity: wsf-ex:Complementor-Seller-B
      role: Complementor
      context: OTCHERE Marketplace
      layer: Supply side
    - entity: wsf-ex:Buyer-Kwesi
      role: User / Prosumer (reviewer)
      context: OTCHERE Marketplace
      layer: Demand side
    - entity: wsf-ex:Algorithmic-Curator
      role: Gatekeeper (automated)
      context: OTCHERE Marketplace
      layer: Curation
    - entity: wsf-ex:Reg-Affairs-Team
      role: Boundary Spanner
      context: External: GDPR regulators, industry bodies
      layer: External interface

  shared_context:
    domain: B2B commerce enablement
    period: 2024-01-01 to present
    regulation: GDPR, industry-specific compliance

  emergent_properties:
    - wsf:Network Effect (Indirect / Cross-Side, dominant)
    - wsf:Lock-In (via review history + integration: emerging)
    - wsf:Ecosystem Health (mature: see metrics below)
    - wsf:Coopetition (Orchestrator ↔ Complementors in services layer)

  structural_primitives:
    - wsf:Platform: OTCHERE Marketplace
    - wsf:Boundary Resources: Seller API, Buyer Web Surface, Mobile SDK
    - wsf:Modularity: High: independent seller + buyer subsystems
    - wsf:Interoperability Standards: REST, OAuth 2.0, OTCHERE Product Schema
    - wsf:Coupling Level: Tight with Sellers, Loose with Buyers

  lifecycle_stage: wsf:Leadership
  health_assessment:
    productivity: 0.82
    robustness: 0.61
    niche_creation: 0.43
    overall: 0.62
    recommendation: "Renew: address niche creation through complementor enablement before leadership erodes."
```

## Narrative

The OTCHERE Platform Ecosystem is a mature digital business ecosystem operated by OTCHERE Inc. It connects sellers (complementors) and buyers (users, some of whom are also prosumers: reviewers, content creators) via the OTCHERE Marketplace platform. OTCHERE Inc acts as Orchestrator, providing the platform, the boundary resources (APIs, SDKs), and the governance rules. The Algorithmic Curator acts as Gatekeeper. The Regulatory Affairs Team acts as Boundary Spanner to GDPR authorities and industry bodies.

The ecosystem exhibits a dominant indirect/cross-side network effect: more sellers attract more buyers, more buyers attract more sellers. Lock-in is emerging through review history and integration depth. Coopetition exists: OTCHERE Inc cooperates with sellers on the supply side and competes with some of them on the services layer.

Lifecycle stage is **Leadership**: the ecosystem is mature but shows early signs of dominator drift (high Productivity, declining Niche Creation). Recommended action: a Self-Renewal initiative focused on complementor enablement to restore Niche Creation rates.

## Cross-references

- `proposals/01-ecosystem/PROPOSAL-01-Ecosystem.md`: parent concept proposal
- `concepts/worked-examples/ecosystem.md`: full concept definition
- `concepts/tier-3/digital-business-ecosystem.md`: the DBE specialisation applied here
- `concepts/health/ecosystem-health.md`: health metric decomposition applied here
- `concepts/lifecycle/lifecycle-stages.md`: lifecycle framework

---

*OTCHERE Platform Ecosystem: the canonical worked example. Status: Baseline.*
