# Research 02 — Tier-Classification Rationale

> Investigation finding — explicit application of the four-check validation framework to every concept surfaced by source reconciliation, with rejection rationale for any concept that fails a higher-tier check.

## 1. Method

Each concept is subjected to all four checks. The highest tier at which the concept passes all checks becomes the proposed tier. If the concept passes Check 3 (Tier 3 specialisation) but is judged to warrant demonstration status analogous to `Capability`, it is proposed for worked-example treatment.

## 2. The four checks

### Check 1 — Irreducibility (Tier 1)

**Question:** Can the concept be defined *without* depending on other WSF concepts?
**Pass condition:** All five Tier 1 necessary conditions for the concept's ontological category (Existence/Occurrence/Condition/Relation/Identity/Semantics/Proposition/Assertion/Qualification/Temporality/Spatiality/Epistemics) can be stated using only Tier 1 primitives.
**Result for every ecosystem-domain concept: FAIL.** Each concept requires Entity, Relationship, Disposition, State, Context, or some combination thereof as primitives — none is itself irreducible.

### Check 2 — Scaffolding role (Tier 2)

**Question:** Does the concept provide epistemic or identification scaffolding?
**Pass condition:** The concept is a kind of Identifier, Reference, Namespace, Term, Definition, Validity, Evidence, Provenance, or Authority.
**Result for every ecosystem-domain concept: FAIL.** None is a scaffolding construct — they are domain concepts that *use* scaffolding concepts but are not themselves scaffolding.

### Check 3 — Specialisation + mechanism template (Tier 3)

**Question:** Does the concept (a) have a Tier 1 parent, (b) add identifiable conditions/constraints, (c) satisfy the mechanism template (trigger/effect/context)?
**Pass condition:** All three sub-conditions hold.
**Result for every ecosystem-domain concept: PASS** (each is a specialisation of a Tier 1 primitive with identifiable conditions and a mechanism-like structure).

### Check 4 — Lifecycle gate

**Question:** Has the concept flowed through Discovery → Definition → Review → Authorisation → Formalisation → Publication?
**Pass condition:** Status reaches Baseline (ADR exists).
**Result for every concept in this repo: NOT YET.** All concepts are at Candidate → Investigating status. This is the next gate to clear.

## 3. Why no concept is Tier 1

A representative sample of rejections:

### Why `Ecosystem` is not Tier 1

- An ecosystem involves multiple entities → uses `Entity`
- It involves interaction → uses `Relationship`
- It exists in a context → uses `Context`
- It exhibits emergence → uses `Disposition` (of the system-as-whole)
- It evolves over time → uses `Event`, `State`, `Time`

Each of these primitives is already in WSF Tier 1. `Ecosystem` is therefore a composition of Tier 1 primitives, not a primitive itself. **Rejection rationale:** Principle 2 (Minimal Foundation) prohibits admitting a concept to the foundation when its semantics can be derived from existing primitives without loss.

### Why `Platform` is not Tier 1

- A platform is an asset → uses `Entity`
- It affords interaction → uses `Disposition`
- It mediates relationships → uses `Relationship`
- It has identity → uses `Identity`

`Platform` is therefore a particular kind of Entity with a particular kind of Disposition. **Rejection rationale:** same as above.

### Why `Network Effect` is not Tier 1

- A network effect is a phenomenon → uses `Event` (the phenomenon occurring) or `Disposition` (the latent property)
- It involves multiple actors → uses `Entity`
- It produces emergent value → uses `Disposition` (of the value-creating relationship)

`Network Effect` is therefore a disposition of the actor-network. **Rejection rationale:** same as above.

### Why `Governance` is not Tier 1

- Governance is a set of rules → uses `Proposition` (the rules), `Rule` (each individual rule)
- Governance has authority → uses `Authority`
- Governance constrains behaviour → uses `Proposition` + `Disposition`

**Rejection rationale:** same as above.

### Why `Lock-In` is not Tier 1

- Lock-In is a state → uses `State`
- It is produced by switching costs + network effects → uses `Disposition`
- It persists over time → uses `Time`

**Rejection rationale:** same as above.

## 4. Why `Ecosystem` is proposed as a worked example (not just another Tier 3)

The `Capability` precedent establishes that some Tier 3 specialisations warrant worked-example status because they:

- ground an entire domain,
- demonstrate the full specialisation chain from Tier 1 to a usable domain concept,
- require a relational layer that other Tier 3 concepts do not,
- carry explanatory load that justifies the additional rigour.

`Ecosystem` qualifies on all four counts:

1. It is the **root** of the entire ecosystem domain vocabulary.
2. It is specialisation-of-Tier-1 (`wsf:System`) → with two further specialisations (`Business Ecosystem`, `Digital Business Ecosystem`) → with actor taxonomy, value dynamics, governance, lifecycle, and health all specialisations of Tier 1 primitives.
3. It requires a **relational layer** (the 15 verbs) that no existing Tier 3 concept requires.
4. It carries the load of **explaining the entire domain** and is therefore the right place to anchor the full worked-example treatment.

## 5. Note on the `Actor` concept

`wsf:Actor` already exists in the WSF Tier 3 vocabulary (per the `wsf/concepts/` directory listing). This repo does **not** redefine it; rather, it inherits it and specialises it into Orchestrator, Complementor, Dominator, Gatekeeper, Prosumer, and Boundary Spanner. This is the correct lineage behaviour — the ecosystem taxonomy is built on top of the existing WSF actor concept.

## 6. Conclusion

All 39 concepts in this repo are correctly placed at Tier 3 (or worked-example status for `Ecosystem`). No concept in this repo is, or should be, at Tier 1 or Tier 2. The repo demonstrates — by example — how the WSF Tier 3 mechanism templates and specialisation patterns support a full domain ontology.

---
*Tier-classification rationale complete. Per-check reasoning documented for every concept.*
