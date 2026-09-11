# Ecosystem Relational Properties (the "Verbs")

> **The 15 object properties (predicates) that connect the classes of the ecosystem ontology.**

This file is a curated supplement to the WSF Semantic Relationship Catalogue. The properties are filed under the namespace prefix **`wsf-rel-eco:`** for clarity, per Open Issue OI-1 in `research/04-modelling-risks/`.

## The 15 predicates

| # | Predicate | Domain | Range | Symmetric | Inverse |
|---|---|---|---|---|---|
| 1 | `wsf-rel-eco:orchestrates` | Actor | Platform | false | `is_orchestrated_by` |
| 2 | `wsf-rel-eco:complements` | Actor | Platform | false | `is_complemented_by` |
| 3 | `wsf-rel-eco:competes_with` | Actor | Actor | true | self-inverse |
| 4 | `wsf-rel-eco:cooperates_with` | Actor | Actor | true | self-inverse |
| 5 | `wsf-rel-eco:exhibits` | Platform | Network Effect | false | `is_exhibited_by` |
| 6 | `wsf-rel-eco:provides` | Orchestrator | Boundary Resource | false | `is_provided_by` |
| 7 | `wsf-rel-eco:allocates_decision_rights_to` | Governance Rule | Role | false | `is_allocated_decision_rights_by` |
| 8 | `wsf-rel-eco:is_coupled_with` | Actor / Relationship | Actor / Relationship | true | self-inverse |
| 9 | `wsf-rel-eco:exchanges_value_with` | Actor | Actor | true | self-inverse |
| 10 | `wsf-rel-eco:co_creates_value_through` | Actor set | Platform | false | `enables_co_creation_for` |
| 11 | `wsf-rel-eco:is_in_lifecycle_stage` | Ecosystem / Platform | Lifecycle Stage | false | `is_lifecycle_stage_of` |
| 12 | `wsf-rel-eco:measured_by` | Ecosystem Health | Health Metric | false | `measures` |
| 13 | `wsf-rel-eco:captures_value_from` | Actor | Value Flow | false | `value_is_captured_by` |
| 14 | `wsf-rel-eco:slips_value_to` | Actor / Ecosystem | Actor | false | `value_slips_from` |
| 15 | `wsf-rel-eco:delegates_governance_to` | Orchestrator | Actor | false | `is_delegated_governance_by` |

## Modelling rules (summary: full text in `research/03-relationship-grammar/`)

1. **R1: Overlapping Roles:** All actor-role predicates MUST be context-scoped (platform, layer, time).
2. **R2: Coopetition:** Modelled as the co-existence of `competes_with` AND `cooperates_with` between the same pair, scoped per layer.
3. **R3: Network Effects are relational:** `exhibits` attaches the effect to the Platform or relationship, NEVER to a single actor.
4. **R4: Lifecycle time-qualified:** Every `is_in_lifecycle_stage` assertion MUST carry time validity.
5. **R5: Coupling requires degree:** Every `is_coupled_with` MUST specify degree (Tight/Loose) and dimension.
6. **R6: Value flow directionality:** Value flow predicates SHOULD carry magnitude when measurable.

## Composition rules (summary)

- `A orchestrates P` ∧ `P exhibits NE` ⊢ A operates in a NE-driven ecosystem
- `A cooperates_with B` ∧ `A competes_with B` (different layers) ⊢ A and B are in coopetition
- `A has high SC` ∧ `P exhibits strong NE` ⊢ A is in Lock-In

## Cross-references

- ADR-WSF-19 (Semantic Relationship Model): the governing metadata schema
- ADR-WSF-25 (Integration Architecture): federation patterns for these predicates
- `research/03-relationship-grammar/`: full grammar

---

*15 ecosystem relational properties filed under `wsf-rel-eco:*` namespace. Status: Baseline.*
