# World Semantic Foundation: Ecosystem Ontology

> **Status:** Candidate / Investigating, per the WSF Change Control Lifecycle.
> **Proposed repository name:** `wsf-ecosystem`, in the `World-Semantic-Foundation` organisation.
> **Upstream location:** https://github.com/World-Semantic-Foundation/wsf-ecosystem

This repository provides a complete, WSF-conformant semantic foundation for the **Ecosystem domain**. It establishes the foundational concept **Ecosystem** as a Tier 3 worked example specialisation of `wsf:System`, and grounds within that concept the full domain ontology required for strategy, platform economics, governance, lifecycle management, and health measurement of business and digital ecosystems.

---

## 1. Scope

The repository contributes nine coherent bodies of content to the WSF foundation.

1. **Three Tier 3 specialisations** of foundational WSF concepts: **Ecosystem** (worked example, parent `wsf:System`), **Business Ecosystem** (specialisation of Ecosystem), **Digital Business Ecosystem** (specialisation of Business Ecosystem).
2. **Six actor roles** as further Tier 3 specialisations of `wsf:Actor`: **Orchestrator** (Keystone), **Complementor** (Niche Player), **Dominator** (degraded variant of Orchestrator), **Gatekeeper** (Curator), **Prosumer** (hybrid), **Boundary Spanner**.
3. **Six structural primitives** as Tier 3 specialisations: **Platform**, **Marketplace**, **Boundary Resources** (Gawer), **Modularity**, **Interoperability Standards**, **Coupling Level**.
4. **Eight value dynamics** as Tier 3 specialisations: **Network Effect** with Direct (Same-Side) and Indirect (Cross-Side) subtypes, **Value Co-creation**, **Value Exchange**, **Value Slippage**, **Switching Costs**, **Lock-In**.
5. **Five governance mechanisms** as Tier 3 specialisations: **Governance** (parent), **Decision Rights Allocation**, **Coopetition**, **Incentive Alignment**, **Trust Mechanisms**.
6. **Four lifecycle stages** per James F. Moore's model: **Birth**, **Expansion**, **Leadership**, **Self-Renewal or Death**.
7. **Three health metrics** per the Iansiti and Levien framework, parented to the **Ecosystem Health** disposition: **Productivity**, **Robustness**, **Niche Creation**.
8. **Fifteen relational properties** (the "verbs") filed under the `wsf-rel-eco:` namespace, governed by six modelling rules that ensure correct treatment of overlapping roles, coopetition, network effects as relational properties (not actor attributes), lifecycle time-qualification, coupling degree, and value flow directionality.
9. **One worked example** drawn from the canonical `OTCHERE Inc` enterprise: the **OTCHERE Platform Ecosystem**, with full health assessment and lifecycle-stage analysis.

## 2. Conceptual foundation

The Ecosystem domain is grounded in four intersecting lines of literature, harmonised through WSF's primitive taxonomy.

- **Ecology and business strategy.** The ecosystem metaphor in management traces to Moore (1993), "Predators and Prey: A New Ecology of Competition," which established both the lifecycle model and the keystone/dominator framing adopted in this repository.
- **Platform economics.** Rochet and Tirole's two-sided market theory, and Iansiti and Levien's "Keystone Advantage" (2004), supply the keystone/dominator role pair and the three health metrics (Productivity, Robustness, Niche Creation).
- **Platform governance.** Gawer's research on platforms and boundary resources supplies the operational construct by which an Orchestrator enables Complementors without reimplementing the platform.
- **Coopetition.** Brandenburger and Nalebuff supply the game-theoretic treatment that requires Coopetition to be modelled as the co-existence of cooperative and competitive predicates between the same actor pair at different layers, not as a single predicate.

The repository reconciles these lines and binds them to WSF Tier 1 primitives (`Entity`, `Relationship`, `Event`, `State`, `Disposition`, `Proposition`, `Assertion`, `Context`, `Time`, `Space`). Every concept in this repository is a Tier 3 specialisation of one of those primitives. No concept is elevated to Tier 1, because every domain concept in scope can be derived from existing primitives without loss of meaning, in conformance with Foundational Principle 2 (Minimal Foundation).

## 3. Why a worked example

The repository designates **Ecosystem** as a Tier 3 worked example, in the same sense that `wsf:Capability` is a worked example in the existing WSF vocabulary. The designation rests on four observations.

- **Ecosystem is the root concept of an entire domain vocabulary.** All other domain concepts (actors, platforms, value dynamics, governance, lifecycle, health) specialise from or relate to it.
- **Ecosystem demonstrates the full specialisation chain.** Tier 1 (`wsf:System`) to Tier 3 worked example (Ecosystem) to further Tier 3 specialisations (Business Ecosystem, Digital Business Ecosystem) and onward to the actor taxonomy, structural primitives, and value dynamics.
- **Ecosystem requires a relational layer.** No other Tier 3 concept in WSF requires fifteen object properties with six modelling rules. The relational grammar is filed under `concepts/relationships/`.
- **Ecosystem carries the explanatory load of the entire domain.** The worked example treatment ensures the concept receives the rigour of ADR-WSF-20 §14 metadata, full positive/negative/borderline cases, and a canonical instance drawn from the OTCHERE example vocabulary.

## 4. Repository layout

| Path | Purpose |
|---|---|
| `proposals/` | Three top-level concept proposals (Ecosystem, Business Ecosystem, Digital Business Ecosystem) formatted for ADR submission |
| `research/` | Four investigation findings: source reconciliation, tier classification, relationship grammar, modelling risks |
| `governance/TIER-CLASSIFICATION-MATRIX.md` | Per-concept tier placement with the validation check applied and rejection rationale for higher tiers |
| `concepts/worked-examples/` | The Ecosystem concept, full ADR-WSF-20 §14 schema |
| `concepts/tier-3/` | Twenty-four Tier 3 concept files, one per concept |
| `concepts/lifecycle/` | Four lifecycle stage files plus a parent index |
| `concepts/health/` | The Ecosystem Health disposition plus the three Iansiti and Levien metric files |
| `concepts/relationships/ecosystem-relational-properties.md` | The fifteen predicates with domain, range, mathematical properties, and modelling rules |
| `examples/otchere-ecosystem/` | The canonical OTCHERE Platform Ecosystem worked example |
| `diagrams/` | Mermaid sources for the concept map and the lifecycle state space, reproducible per CR-WSF-17 Rev.1 §14 |

## 5. Tier-classification summary

The full reasoning per concept is recorded in `governance/TIER-CLASSIFICATION-MATRIX.md`. The headline.

- **Tier 1:** no new concepts proposed. Every domain concept composes from existing Tier 1 primitives without loss of meaning.
- **Tier 2:** no new constructs proposed. Epistemic scaffolding needs (identifier, namespace, term, definition, evidence, provenance, authority) are already covered by the existing WSF Tier 2 vocabulary.
- **Tier 3:** twenty-four concepts, each parented to a Tier 1 primitive with identifiable conditions, constraints, and mechanism template (trigger, effect, applicable contexts).
- **Worked example:** one (Ecosystem), with the rationale set out in §3.

The tier-classification matrix is the audit trail: every placement cites the validation check applied, and every rejected promotion to a higher tier cites the irreducibility failure.

## 6. Standards of practice

The repository is governed by the following standards, which apply to every artifact in this repository and to future contributions.

- **Example convention.** All examples use the canonical enterprise `OTCHERE Inc` and the canonical individual `Kwesi`. ACME is prohibited per the WSF Example Consistency Principle (LOCKED-PICKS v9 §13).
- **Concept schema.** Every concept file follows the ADR-WSF-20 §14 metadata schema (identification, classification, definition, conditions, constraints, relationships, examples, context, governance, provenance).
- **Tone.** Prose is normative: it states the concept, not the conversation that produced it. Artifacts read as independent normative documents, not as records of dialogue.
- **Punctuation.** Em dashes and en dashes are not used. Colons, semicolons, commas, and parentheses carry the structural load that em and en dashes otherwise would.
- **Punctuation variants (Chinese, Japanese, Korean).** Full-width em dash (U+2014) and en dash (U+2013) are likewise excluded.
- **Change control.** Every semantic change flows through the WSF Change Control Lifecycle (Discovery, Definition, Review, Authorisation, Formalisation, Publication, Specialisation, Instantiation, Assertion, Evidence, Validation, Governance, Version/Deprecation). All Change Requests (CRs), submittals, and research actions are logged as GitHub Issues in the relevant repository, and factored into the ongoing plans and work of the Ecosystem Working Group.

## 7. Status and next moves

This repository is at status **Candidate / Investigating** in WSF terms. Every concept is at the corresponding lifecycle stage. The next moves are recorded and tracked as GitHub Issues in the `World-Semantic-Foundation/wsf-ecosystem` repository.

1. Reconcile this workspace against the four layered tier-validation checks documented in `research/02-tier-classification/`.
2. File the three top-level proposals under `proposals/` as investigation findings, preparatory to raising ADRs.
3. Draft and raise ADRs for Ecosystem (worked example), the actor taxonomy, the value dynamics, and the structural primitives.
4. Draft and raise Change Requests for the additions to `wsf-spec/` (the fifteen `wsf-rel-eco:` predicates, the SHACL shapes, the JSON Schema, the Protobuf messages, the Turtle vocabulary, and the OWL/RDF skeleton for the twenty-four classes).
5. Mirror the OTCHERE worked example to `wsf-examples/` for cross-repo consistency.

## 8. Provenance and references

- **Moore, J. F.** (1993), "Predators and Prey: A New Ecology of Competition," *Harvard Business Review*. Source of the ecosystem metaphor and lifecycle model.
- **Iansiti, M., and Levien, R.** (2004), *The Keystone Advantage*. Source of the keystone/dominator role pair and the Productivity, Robustness, Niche Creation metrics.
- **Gawer, A.** Research on platforms and boundary resources. Source of the Boundary Resources construct.
- **Rochet, J. C., and Tirole, J.** Two-sided market theory. Source of the Marketplace foundations.
- **Brandenburger, A., and Nalebuff, B.** Coopetition. Source of the cooperative-competitive co-existence treatment.
- **Source artifacts in this repository.** `research/01-source-reconciliation/FINDING-Source-Reconciliation.md` provides the full lineage mapping between the upstream source documents and this repository's concept files.

---

*This repository is governed by the World Semantic Foundation's 12 Foundational Principles, its 27 Architectural Decision Records, and the Change Control Lifecycle. Contributions flow through ADRs and CRs filed as GitHub Issues.*
