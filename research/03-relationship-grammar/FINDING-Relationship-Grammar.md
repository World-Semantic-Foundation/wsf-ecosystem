# Research 03: Relationship Grammar

> Investigation finding: the 15 relational properties (the "verbs") of ecosystem ontology, grounded against the WSF Semantic Relationship Model (ADR-WSF-19) and prepared for inclusion in the WSF Semantic Relationship Catalogue.

## 1. Purpose

A class taxonomy is meaningless without a relationship grammar. The 15 relational properties below connect the 24 class concepts in this repo. Each property follows the ADR-WSF-19 metadata schema (semantic_id, domain, range, mathematical properties, inverse, governance).

## 2. The 15 relational properties

### 2.1 `wsf-rel:orchestrates`

- **Domain:** `Actor` (typically Orchestrator)
- **Range:** `Platform`
- **Symmetric:** false
- **Transitive:** false
- **Inverse:** `wsf-rel:is_orchestrated_by`
- **Description:** The Orchestrator provides the core platform, sets standards, and manages ecosystem health.
- **Example:** Apple `orchestrates` iOS.

### 2.2 `wsf-rel:complements`

- **Domain:** `Actor` (typically Complementor)
- **Range:** `Platform`
- **Symmetric:** false
- **Transitive:** false
- **Inverse:** `wsf-rel:is_complemented_by`
- **Description:** An actor creates value by adding specialised products or services to the platform.
- **Example:** A third-party developer `complements` iOS.

### 2.3 `wsf-rel:competes_with`

- **Domain:** `Actor`
- **Range:** `Actor`
- **Symmetric:** true (if A competes with B, then B competes with A)
- **Transitive:** false
- **Inverse:** self-inverse
- **Description:** Two actors compete within the same niche or value layer.
- **Example:** Spotify `competes_with` Apple Music.
- **Context scoping required:** the niche and layer MUST be asserted.

### 2.4 `wsf-rel:cooperates_with`

- **Domain:** `Actor`
- **Range:** `Actor`
- **Symmetric:** true
- **Transitive:** false
- **Inverse:** self-inverse
- **Description:** Two actors cooperate to grow the total market or to deliver joint value.
- **Example:** Apple `cooperates_with` developers on the App Store.
- **Context scoping required:** the value layer and time period MUST be asserted.

### 2.5 `wsf-rel:exhibits`

- **Domain:** `Platform`
- **Range:** `Network Effect` (with subtype: Direct or Indirect)
- **Symmetric:** false
- **Transitive:** false
- **Inverse:** `wsf-rel:is_exhibited_by`
- **Description:** The platform exhibits a particular kind of network effect as a property of its actor relationships.
- **Example:** iOS `exhibits` Cross-Side Network Effects.

### 2.6 `wsf-rel:provides`

- **Domain:** `Orchestrator` (or delegated actor)
- **Range:** `Boundary Resource`
- **Symmetric:** false
- **Transitive:** false
- **Inverse:** `wsf-rel:is_provided_by`
- **Description:** The Orchestrator provides Boundary Resources to enable complementors.
- **Example:** Apple `provides` the iOS SDK.

### 2.7 `wsf-rel:allocates_decision_rights_to`

- **Domain:** `Governance Rule` (or Decision Rights Allocation)
- **Range:** `Role` (typically Orchestrator or Gatekeeper)
- **Symmetric:** false
- **Transitive:** false
- **Inverse:** `wsf-rel:is_allocated_decision_rights_by`
- **Description:** A governance rule allocates decision rights to a role.
- **Example:** The App Store Review Guidelines `allocates_decision_rights_to` the Gatekeeper.

### 2.8 `wsf-rel:is_coupled_with`

- **Domain:** `Actor` (or Relationship)
- **Range:** `Actor` (or Relationship)
- **Symmetric:** true
- **Transitive:** false (coupling is a pairwise property, not a transitive one)
- **Inverse:** self-inverse
- **Description:** Two actors (or relationships) exhibit a specified Coupling Level (Tight or Loose).
- **Example:** Fulfillment partners `is_coupled_with` Amazon (Tight).
- **Context scoping required:** the value layer and the coupling degree MUST be asserted.

### 2.9 `wsf-rel:exchanges_value_with`

- **Domain:** `Actor`
- **Range:** `Actor`
- **Symmetric:** true (value exchange is bilateral)
- **Transitive:** false
- **Inverse:** self-inverse
- **Description:** Two actors exchange value (money, goods, services, data, attention).
- **Example:** Buyers `exchanges_value_with` Sellers via Marketplace.

### 2.10 `wsf-rel:co_creates_value_through`

- **Domain:** `Actor set` (typically a Platform's actor community)
- **Range:** `Platform`
- **Symmetric:** false
- **Transitive:** false
- **Inverse:** `wsf-rel:enables_co_creation_for`
- **Description:** A set of actors co-create value through a platform.
- **Example:** Developers `co_creates_value_through` the App Store.

### 2.11 `wsf-rel:is_in_lifecycle_stage`

- **Domain:** `Ecosystem` (or Platform)
- **Range:** `Lifecycle Stage`
- **Symmetric:** false
- **Transitive:** false
- **Inverse:** `wsf-rel:is_lifecycle_stage_of`
- **Description:** The ecosystem is currently in a specified lifecycle stage.
- **Example:** OTCHERE Marketplace `is_in_lifecycle_stage` Leadership.

### 2.12 `wsf-rel:measured_by`

- **Domain:** `Ecosystem Health`
- **Range:** `Health Metric` (Productivity, Robustness, or Niche Creation)
- **Symmetric:** false
- **Transitive:** false
- **Inverse:** `wsf-rel:measures`
- **Description:** Ecosystem health is measured by a specified metric.
- **Example:** Ecosystem Health `measured_by` Niche Creation rate.

### 2.13 `wsf-rel:captures_value_from`

- **Domain:** `Actor` (typically Orchestrator)
- **Range:** `Value Exchange` (or value flow)
- **Symmetric:** false
- **Transitive:** false
- **Inverse:** `wsf-rel:value_is_captured_by`
- **Description:** The actor captures value from a value flow.
- **Example:** OTCHERE Inc `captures_value_from` Marketplace take rate.

### 2.14 `wsf-rel:slips_value_to`

- **Domain:** `Actor` (or ecosystem)
- **Range:** `Actor` (typically external: competitor, free-rider, regulator)
- **Symmetric:** false
- **Transitive:** false
- **Inverse:** `wsf-rel:value_slips_from`
- **Description:** Value generated within the ecosystem escapes capture and flows to an external actor.
- **Example:** Free-riders `slips_value_to` competitors.

### 2.15 `wsf-rel:delegates_governance_to`

- **Domain:** `Orchestrator`
- **Range:** `Actor` (typically Gatekeeper)
- **Symmetric:** false
- **Transitive:** false
- **Inverse:** `wsf-rel:is_delegated_governance_by`
- **Description:** The Orchestrator delegates specified governance functions to another actor.
- **Example:** OTCHERE Inc `delegates_governance_to` the Algorithmic Curator.

## 3. Modelling rules (governing the use of these predicates)

### Rule R1: Overlapping Roles require context scoping

All actor-role predicates (`orchestrates`, `complements`, `delegates_governance_to`, etc.) MUST be scoped to a context (platform, layer, time). Apple is Orchestrator of iOS and Complementor to hardware suppliers: these are different assertions on different platforms and layers.

### Rule R2: Coopetition is a co-existence of competing and cooperating predicates

Modelling coopetition requires asserting BOTH `competes_with` AND `cooperates_with` between the same actor pair, scoped to different layers. The pair is in coopetition iff the two predicates coexist with non-overlapping layer contexts.

### Rule R3: Network Effects are relational properties, not actor attributes

`exhibits` MUST attach the Network Effect to the Platform (or actor-relationship), not to a single actor. Network effects are emergent properties of the actor network.

### Rule R4: Lifecycle stage assertions MUST be time-qualified

Every `is_in_lifecycle_stage` assertion MUST carry a time validity period. An ecosystem was in Birth in 2018 and is in Leadership in 2026: both can be historically true.

### Rule R5: Coupling Level requires degree assertion

Every `is_coupled_with` assertion MUST specify the degree (Tight or Loose) and the dimension (technical, contractual, data, etc.).

### Rule R6: Value flow predicates require directionality and magnitude

Every `exchanges_value_with`, `captures_value_from`, and `slips_value_to` assertion SHOULD carry directionality (inherently from domain/range) and magnitude (when measurable).

## 4. Composition rules

Some predicates compose:

- `A orchestrates P` ∧ `P exhibits NE` ⊢ `A operates in a NE-driven ecosystem` (derived, not new predicate)
- `A cooperates_with B` ∧ `A competes_with B` ∧ same pair, different layers ⊢ `A and B are in coopetition` (derived state)
- `A has high SC` ∧ `P exhibits strong NE` ⊢ `A is in Lock-In` (derived state)

These compositions SHOULD be expressible via inference rules in the Semantic Engine (per CR-WSF-17 Rev.1 §17 Simulation pattern).

## 5. Conclusion

The 15 relational properties, plus the 6 modelling rules, form the complete relationship grammar for the ecosystem domain. They are filed for inclusion in the WSF Semantic Relationship Catalogue and in `wsf-spec`'s Turtle/JSON-LD/Protobuf serialisations.

---
*Relationship grammar complete. Ready for ADR formalisation.*
