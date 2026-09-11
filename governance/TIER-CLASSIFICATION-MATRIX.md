# Tier-Classification Matrix: Ecosystem Domain

> The full mapping of every concept surfaced by ADR-CONCEPTS-01.md and VOCAB-000.md (v2.0) to its proposed WSF tier, with the validation checks applied per concept and explicit rejection of Tier 1 status with reasoning.

## Validation framework: recap

Every concept passes through four layered checks before tier placement is ratified:

1. **Irreducibility (ADR-WSF-17 + Principle 2)**: Can the concept be defined *without* depending on other WSF concepts? If yes → Tier 1 candidate. If it can be composed from existing primitives without loss → **not Tier 1**.
2. **Scaffolding role (ADR-WSF-20 §12)**: Does the concept provide epistemic or identification scaffolding (identifier, namespace, term, definition, validity, evidence, provenance, authority)? If yes → Tier 2.
3. **Specialisation + mechanism template (ADR-WSF-04, ADR-WSF-09, ADR-WSF-20 §12)**: Does the concept (a) have a Tier 1 parent, (b) add identifiable conditions/constraints, (c) satisfy the mechanism template (trigger/effect/context)? If yes → Tier 3.
4. **Lifecycle gate (Change Control Lifecycle + Semantic Status Model)**: Status must reach Baseline (ADR filed) before downstream may specialise; Final only after CR implementation verified.

## Headline outcome

**Zero Tier 1, zero Tier 2, twenty-eight Tier 3, one worked-example (Ecosystem itself).** Every domain concept in this repo fails the irreducibility test for Tier 1, is not a scaffolding construct for Tier 2, and satisfies the specialisation + mechanism template for Tier 3.

## Per-concept matrix

### Top-level (proposals folder)

| Concept | Proposed Tier | Parent | Validation check passed | Rationale (one line) |
|---|---|---|---|---|
| **Ecosystem** | **Worked Example** (analogous to `Capability`) | `wsf:System` | Checks 3 + 4 | A complex system of interacting entities exhibiting emergent properties. Not irreducible (composes from Entity + Relationship + System + Context). Elevated to worked-example status because it is the demonstration that the Tier 3 specialisation chain can ground an entire domain. |
| **Business Ecosystem** | Tier 3 (specialisation) | `wsf:Ecosystem` | Check 3 | Specialises Ecosystem with domain constraints (organisational actors, value creation, shared fate). |
| **Digital Business Ecosystem** | Tier 3 (specialisation) | `wsf:Business Ecosystem` | Check 3 | Specialises Business Ecosystem with the digital-medium constraint. |

### Actors (Section 3.1 of VOCAB-000 v2.0)

| Concept | Proposed Tier | Parent | Rationale |
|---|---|---|---|
| **Actor** | Tier 3 | `wsf:Entity` | The root actor class: autonomous goal-pursuing entity. Already has parallel in WSF `wsf:Actor` (existing). Cross-validate. |
| **Orchestrator (Keystone)** | Tier 3 | `wsf:Actor` | Specialised actor role providing core platform and standards. |
| **Complementor (Niche Player)** | Tier 3 | `wsf:Actor` | Specialised actor role adding value to a core platform. |
| **Dominator (Keystone Competitor)** | Tier 3 | `wsf:Orchestrator` | Degraded variant of Orchestrator through value extraction: modelled as a specialisation so the keystone-to-dominator drift can be expressed as a state transition. |
| **Gatekeeper / Curator** | Tier 3 | `wsf:Actor` (functional role) | Specialised governance function; typically delegated by Orchestrator. |
| **Prosumer** | Tier 3 | `wsf:Actor` | Hybrid class demonstrating non-mutual exclusion of actor roles. |
| **Boundary Spanner** | Tier 3 | `wsf:Actor` | Interface role connecting the ecosystem system boundary to its environment. |

### Structure (Section 3.2)

| Concept | Proposed Tier | Parent | Rationale |
|---|---|---|---|
| **Platform** | Tier 3 | `wsf:Entity` | Foundational asset: technological/brand/infrastructural: for ecosystem interactions. |
| **Marketplace** | Tier 3 | `wsf:Platform` | Subtype specialising Platform with transaction intermediation. |
| **Boundary Resources** | Tier 3 | `wsf:Entity` | Concrete, engineered embodiment of the Platform primitive (APIs, SDKs, etc.). |
| **Modularity** | Tier 3 | `wsf:Disposition` | Architectural property enabling decomposition; modelled as a disposition of the platform. |
| **Interoperability Standards** | Tier 3 | `wsf:Proposition` (rules) | Shared protocols and rules: modelled as a specialisation of Rule. |
| **Coupling Level** | Tier 3 | `wsf:Relationship` (descriptive property) | Descriptive property of value-exchange relationships. |

### Value dynamics (Section 3.3)

| Concept | Proposed Tier | Parent | Rationale |
|---|---|---|---|
| **Network Effect** | Tier 3 | `wsf:Disposition` | Phenomenon where value increases with adoption: an emergent disposition of the actor-network. |
| **Direct (Same-Side) Network Effect** | Tier 3 | `wsf:Network Effect` | Subtype refinement. |
| **Indirect (Cross-Side) Network Effect** | Tier 3 | `wsf:Network Effect` | Subtype refinement. |
| **Value Co-creation** | Tier 3 | `wsf:Proposition` | The proposition that value is jointly generated by multiple actors. |
| **Value Exchange** | Tier 3 | `wsf:Relationship` | The fundamental edge of the ecosystem graph. |
| **Value Slippage** | Tier 3 | `wsf:Event` | The occurrence by which value escapes capture. |
| **Switching Costs** | Tier 3 | `wsf:Disposition` | The friction-faced-when-leaving disposition. |
| **Lock-In** | Tier 3 | `wsf:State` | The emergent state produced by high switching costs + strong network effects. |

### Governance (Section 3.4)

| Concept | Proposed Tier | Parent | Rationale |
|---|---|---|---|
| **Governance** | Tier 3 | `wsf:Proposition` (rules set) | The meta-rule-set governing ecosystem behaviour. |
| **Decision Rights Allocation** | Tier 3 | `wsf:Relationship` | The relational act of distributing authority. |
| **Coopetition** | Tier 3 | `wsf:State` (and a relational property) | The co-existence state of cooperative + competitive relations between the same actor pair. |
| **Incentive Alignment** | Tier 3 | `wsf:Disposition` | The mechanism ensuring self-interested actions benefit the whole. |
| **Trust Mechanisms** | Tier 3 | `wsf:System` (institutional/algorithmic) | The systems reducing transaction costs between strangers. |

### Lifecycle (Section 3.5)

| Concept | Proposed Tier | Parent | Rationale |
|---|---|---|---|
| **Birth** | Tier 3 | `wsf:State` | Lifecycle stage: value proposition definition. |
| **Expansion** | Tier 3 | `wsf:State` | Lifecycle stage: supply/demand scaling. |
| **Leadership / Authority** | Tier 3 | `wsf:State` | Lifecycle stage: mature stability and defence. |
| **Self-Renewal or Death** | Tier 3 | `wsf:State` | Lifecycle stage: the bifurcation point. |

### Health metrics (Section 3.6)

| Concept | Proposed Tier | Parent | Rationale |
|---|---|---|---|
| **Ecosystem Health** | Tier 3 | `wsf:Disposition` | Parent health concept. |
| **Productivity** | Tier 3 | `wsf:Measure` | Iansiti and Levien metric. |
| **Robustness** | Tier 3 | `wsf:Measure` | Iansiti and Levien metric. |
| **Niche Creation** | Tier 3 | `wsf:Measure` | Iansiti and Levien metric. |

### Concepts rejected for promotion

| Concept | Why rejected for higher tier |
|---|---|
| Ecosystem as Tier 1 | Composes from `Entity` + `Relationship` + `System` + `Context` without loss of meaning: fails Principle 2 (Minimal Foundation). |
| Network Effect as Tier 1 | Composes from `Disposition` (of an actor-network) + `State` (of the value-creating relation): fails irreducibility. |
| Platform as Tier 1 | Composes from `Entity` (the asset) + `Disposition` (its affordances): fails irreducibility. |
| Governance as Tier 1 | Composes from `Proposition` (rules) + `Authority` (who enforces): fails irreducibility. |
| Lock-In as Tier 1 | Composes from `State` (emergent) + `Disposition` (of switching costs): fails irreducibility. |

## Summary count

- **Worked examples:** 1 (Ecosystem)
- **Tier 3 specialisations:** 28 (counting both parent and child subtypes for Network Effects and Lifecycle)
- **Tier 2 proposed:** 0 (no new scaffolding constructs needed; existing WSF vocabulary covers identifier, namespace, term, definition, evidence, provenance, authority)
- **Tier 1 proposed:** 0 (deliberately: Principle 2)
