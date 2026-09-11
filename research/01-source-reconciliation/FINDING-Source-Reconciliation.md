# Research 01 — Source Reconciliation

> Investigation finding (F-NNN, to be assigned) — reconciles the two source documents (ADR-CONCEPTS-01.md and VOCAB-000.md v2.0) and establishes the lineage from which this repo's concepts are drawn.

## 1. Source documents

| Source | Type | Date | Author | Status |
|---|---|---|---|---|
| `ADR-CONCEPTS-01.md` | Concept catalog (raw) | — | Strategy/ontology author (Moore/Gawer/Iansiti-Levien lineage) | Source material |
| `VOCAB-000.md` (v2.0) | Harmonised vocabulary (drafted v2.0 from v1.0 + ADR-CONCEPTS-01) | v2.0 | Vocabulary author | Draft for reconciliation |

## 2. Lineage of each concept

| # | Concept | Source in ADR-CONCEPTS-01 | Source in VOCAB-000 v2.0 | Status after reconciliation |
|---|---|---|---|---|
| 1 | Ecosystem | §1 (implicit, "ecosystem ontology") | §2.1 | New — formalised |
| 2 | Business Ecosystem | §1 ("A Business Ecosystem is non-linear…") | §2.2 | New — formalised |
| 3 | Digital Ecosystem | — | §2.3 | New — formalised |
| 4 | Digital Business Ecosystem | — | §2.4 | New — formalised |
| 5 | Actor (Node) | §1 (implicit) | §3.1.1 | Already exists in WSF as `wsf:Actor`; cross-validate |
| 6 | Orchestrator (Keystone) | §1.1 | §3.1.2 | New — formalised |
| 7 | Complementor (Niche Player) | §1.1 | §3.1.3 | New — formalised |
| 8 | Dominator (Keystone Competitor) | §1.1 | §3.1.4 | New — formalised |
| 9 | Gatekeeper / Curator | §1.1 | §3.1.5 | New — formalised |
| 10 | Prosumer | §1.1 | §3.1.6 | New — formalised |
| 11 | Boundary Spanner | §1.1 | §3.1.7 | New — formalised |
| 12 | Platform | §2.1 | §3.2.1 | New — formalised |
| 13 | Marketplace | — (referenced as implicit) | §3.2.2 | New — formalised |
| 14 | Boundary Resources | §2.1 (Gawer reference) | §3.2.3 | New — formalised |
| 15 | Modularity | §2.1 | §3.2.4 | New — formalised |
| 16 | Interoperability Standards | §2.1 | §3.2.5 | New — formalised |
| 17 | Coupling Level | §2.1 | §3.2.6 | New — formalised |
| 18 | Network Effect | §3 (intro) | §3.3.1 | New — formalised (refined into subtypes) |
| 19 | Direct (Same-Side) Network Effect | §3.1 | §3.3.1 subtypes | New — formalised |
| 20 | Indirect (Cross-Side) Network Effect | §3.1 | §3.3.1 subtypes | New — formalised |
| 21 | Value Co-creation | §3.2 | §3.3.2 | New — formalised |
| 22 | Value Exchange | — (implicit) | §3.3.3 | New — formalised |
| 23 | Value Slippage | §3.2 | §3.3.4 | New — formalised |
| 24 | Switching Costs | §3.2 | §3.3.5 | New — formalised |
| 25 | Lock-In | §3.2 | §3.3.6 | New — formalised |
| 26 | Governance | §4 (intro) | §3.4.1 | New — formalised |
| 27 | Decision Rights Allocation | §4.1 | §3.4.2 | New — formalised |
| 28 | Coopetition | §4.2 | §3.4.3 | New — formalised |
| 29 | Incentive Alignment | §4.3 | §3.4.4 | New — formalised |
| 30 | Trust Mechanisms | §4.4 | §3.4.5 | New — formalised |
| 31 | Birth (lifecycle stage) | §5.1 | §3.5.1 | New — formalised |
| 32 | Expansion (lifecycle stage) | §5.2 | §3.5.2 | New — formalised |
| 33 | Leadership / Authority (lifecycle stage) | §5.3 | §3.5.3 | New — formalised |
| 34 | Self-Renewal or Death (lifecycle stage) | §5.4 | §3.5.4 | New — formalised |
| 35 | Ecosystem Health | §6 (intro) | §3.6.1 | New — formalised |
| 36 | Productivity | §6.1 | §3.6.2 | New — formalised |
| 37 | Robustness | §6.2 | §3.6.3 | New — formalised |
| 38 | Niche Creation | §6.3 | §3.6.4 | New — formalised |
| 39 | Relational properties (the "verbs") | §7 | §4 | New — formalised (15 predicates) |
| 40 | Overlapping Roles principle | §7 (caveat) | §3.1 caveat + §4 ⚠️ | Modelling rule, not a concept |

**Total distinct concepts proposed for the ecosystem repo: 39** (3 top-level + 6 actor taxonomy entries beyond `Actor` + 6 structure + 8 value dynamics + 5 governance + 4 lifecycle + 4 health + 1 `Ecosystem Health` parent + 15 relational properties). Of these, 15 relational properties are predicates (object properties) rather than classes, so the *class* count is **24** and the *predicate* count is **15**.

## 3. Gap analysis findings

### Found in ADR-CONCEPTS-01 but not in VOCAB-000 v1.0 (resolved by v2.0)

- Boundary Resources, Dominator, Gatekeeper, Prosumer, Boundary Spanner
- Modularity, Interoperability Standards, Coupling Level
- Direct vs Indirect Network Effects subtypes
- Value Slippage, Switching Costs, Lock-In
- Decision Rights Allocation, Incentive Alignment, Trust Mechanisms
- Lifecycle stages (explicit entries)
- Health metrics decomposition (Productivity, Robustness, Niche Creation)
- Relational Properties (the "verbs") — *the single largest structural addition*
- Overlapping Roles principle (modelling caveat)

### Found in VOCAB-000 but not in ADR-CONCEPTS-01

- Ecosystem Health (parent concept — decomposed in v2.0)
- Value Exchange (separate from Value Co-creation)
- Marketplace (explicit subtype of Platform)
- Digital Ecosystem (general) — separate from Digital Business Ecosystem

### Where v2.0 weakened or changed meaning

- "Keystone" in ADR-CONCEPTS-01 is treated as identical to "Orchestrator"; v2.0 makes the keystone-to-dominator drift explicit and treats Dominator as a separate specialisation of Orchestrator (correct modelling — they are different kinds of behaviour).
- "Coopetition" was mentioned only in §2 foundations in v1.0; v2.0 promotes it to a full entry and recognises it as both a state and a relational property pair (correct — Brandenburger & Nalebuff treat it as a simultaneous cooperative-competitive stance).

## 4. Authoritative literature cited

| Source | Cited in | Authority |
|---|---|---|
| Moore (1993) "Predators and Prey" | Both | Original ecosystem metaphor + lifecycle model |
| Iansiti & Levien (2004) "The Keystone Advantage" | Both | Keystone/dominator roles; productivity/robustness/niche-creation metrics |
| Gawer (research on platforms & boundary resources) | ADR-CONCEPTS-01 §2.1; v2.0 §3.2.3 | Boundary Resources construct |
| Rochet & Tirole (two-sided markets) | v2.0 references | Marketplace foundations |
| Brandenburger & Nalebuff (Co-opetition) | v2.0 references | Coopetition construct |

## 5. Conclusion for reconciliation

Both source documents are mutually consistent. ADR-CONCEPTS-01 is the raw strategic framing; VOCAB-000 v2.0 is the harmonised engineering-grade vocabulary with the relational layer added. The repo formalises both as WSF Tier 3 concepts and predicates, with `Ecosystem` itself elevated to worked-example status.

---
*Reconciliation complete. No contradictions found. Both sources agree on the substance; v2.0 has done the work of class-relationship integration that ADR-CONCEPTS-01 left to the implementer.*
