# Research 04 — Modelling Risks

> Investigation finding — explicit catalogue of the modelling risks in formalising the ecosystem domain against WSF, with mitigation strategies.

## 1. Risk register

### Risk R1 — Over-extending the specialisation chain

**Description:** The ecosystem domain is large, and there is a temptation to recursively specialise every concept (e.g., `Prosumer` → `Content Prosumer` → `Video Content Prosumer`). Each level adds semantic load but reduces reusability.
**Impact:** Concept explosion; maintenance burden; conformance violations.
**Mitigation:** Apply Principle 2 (Minimal Foundation) recursively — only specialise when the new semantics cannot be derived from context assertions on the parent.

### Risk R2 — Conflating Domain with Foundational semantics

**Description:** In the heat of vocabulary harmonisation, it is tempting to promote widely-used domain concepts (e.g., `Platform`, `Ecosystem`) to Tier 1 status.
**Impact:** Violates Principle 2; destabilises the foundation; makes downstream consumers' lives harder.
**Mitigation:** All ecosystem concepts are forced through the four-check validation framework before tier assignment; the tier-classification matrix in `governance/TIER-CLASSIFICATION-MATRIX.md` is the audit trail.

### Risk R3 — Modelling Coopetition as a single predicate

**Description:** Coopetition is fundamentally a *state* arising from the co-existence of cooperative AND competitive relationships between the same actor pair at different layers.
**Impact:** If modelled as a single predicate, the semantic distinction between the two relationship types is lost.
**Mitigation:** Per Rule R2 in `research/03-relationship-grammar/`, coopetition is modelled as the co-existence of `cooperates_with` and `competes_with`, scoped per layer.

### Risk R4 — Modelling Network Effects as actor attributes

**Description:** Network Effects are emergent properties of the actor network, not attributes of any single firm.
**Impact:** Conflating them with firm attributes loses the relational and emergent nature.
**Mitigation:** Per Rule R3 in the relationship grammar, `exhibits` attaches the Network Effect to the Platform (or the relationship), not to any actor.

### Risk R5 — Ignoring role overlap

**Description:** Apple is simultaneously Orchestrator of iOS, Complementor of hardware suppliers, and Competitor of its own App Store developers in services. Treating any actor as having a single role loses essential information.
**Impact:** Incomplete models; incorrect inferences; misaligned governance.
**Mitigation:** Per Rule R1, all actor-role predicates are context-scoped to (platform, layer, time).

### Risk R6 — Treating Lifecycle as linear

**Description:** Moore's lifecycle (Birth → Expansion → Leadership → Self-Renewal/Death) is sometimes presented as strictly linear.
**Impact:** Linear treatment hides the possibility of regression (Expansion → Birth after a major shock), parallel stages (Self-Renewal during Leadership), and multi-ecosystem dynamics.
**Mitigation:** Model lifecycle as a state space with allowed transitions, not a single directed path. The four stages are STATES; transitions between them are themselves EVENTS that can be asserted with provenance.

### Risk R7 — Decomposing Health too far

**Description:** The three Iansiti–Levien metrics (Productivity, Robustness, Niche Creation) can be further decomposed indefinitely (Productivity → transaction velocity, conversion rate, throughput, …).
**Impact:** Metric proliferation; measurement burden; comparability loss.
**Mitigation:** The three top-level metrics are normative; their sub-metrics are domain-specific and live in DOWNSTREAM specialisations (e.g., an OpenDEA maturity assessment), not in WSF.

### Risk R8 — Mis-modelling Boundary Resources as a separate concept

**Description:** Boundary Resources could be modelled as a kind of Platform (which would make them identical to the Platform).
**Impact:** Loss of the operational distinction — Boundary Resources are the *interfaces* that the Platform provides, not the Platform itself.
**Mitigation:** Boundary Resources are a separate Tier 3 specialisation of `Entity` (the concrete, engineered embodiment of the Platform's affordances), related to Platform via `is_provided_by` Orchestrator.

### Risk R9 — Treating Value Exchange and Value Co-creation as identical

**Description:** Value Exchange is the bilateral flow of value between two actors; Value Co-creation is the multi-actor generation of value through a platform.
**Impact:** Conflating them collapses two distinct phenomena — transactional vs. generative.
**Mitigation:** Distinct concepts with distinct parents: Value Exchange ⊂ `Relationship`; Value Co-creation ⊂ `Proposition` (the proposition that value is jointly created).

### Risk R10 — Forgetting the Overlapping Roles principle in federation

**Description:** When federating with external ontologies (Schema.org, SKOS, TM Forum), the external concepts often assume single-role actors.
**Impact:** Loss of information in federation; incorrect mappings.
**Mitigation:** Federation mappings (per ADR-WSF-25) MUST preserve the context-scoping structure. Schema.org `Organization` → WSF `Actor`, with Orchestrator/Complementor/etc. as scoped specialisations, not flat alternatives.

## 2. Risks rejected (false positives)

The following concerns were raised and dismissed after investigation:

| Concern | Why dismissed |
|---|---|
| "Ecosystem should be Tier 1 because it is universal." | Universality of use ≠ irreducibility of semantics. Ecosystem composes from Tier 1 primitives without loss. |
| "Lock-In should be a mechanism, not a state." | Per ADR-WSF-17, Lock-In is the emergent state produced by switching costs + network effects. A state is the correct ontological category. |
| "Boundary Spanner is just an actor, not a role." | All actor classes in this repo are role-as-actor. Boundary Spanner is the role whose defining characteristic is interface management. |
| "Coopetition is too soft to formalise." | Brandenburger & Nalebuff's game-theoretic treatment shows it can be formalised as the intersection of two relationship sets. Rule R2 captures this. |
| "Lifecycle stages are too strategy-specific." | They are generalisable to any ecosystem (biological, technological, business) — Moore's model is intentionally cross-domain. |

## 3. Open issues for ADR resolution

The following modelling decisions cannot be made at this repo level and require upstream ADR input:

- **OI-1:** Should the WSF Semantic Relationship Catalogue be extended with the 15 ecosystem predicates as a single named family (`wsf-rel-eco:*`)? Or should they be absorbed into the existing `wsf-rel:*` namespace? (Recommended: `wsf-rel-eco:*` for clarity.)
- **OI-2:** Should `wsf:Actor` be deprecated in favour of `wsf:Role` (the more general concept that includes Actor)? Or should `Actor` remain as the actor-as-entity class? (Recommended: keep `Actor`; add `Role` as a separate concept for contextual identity.)
- **OI-3:** Should Coopetition be modelled as a State (a `State` of an actor pair) or as a relational pattern (a co-existence of predicates)? The repo currently models both — the State aspect is the precondition for the relational pattern. (Recommended: formalise as State, with the relational pattern as the operationalisation.)

## 4. Conclusion

The modelling risks are well-understood and mitigations are in place. The open issues are flagged for upstream ADR resolution and do not block local concept authoring.

---
*Modelling risks catalogue complete. Mitigations documented. Open issues surfaced.*
