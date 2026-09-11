# World Semantic Foundation — Ecosystem Ontology Repo

> **Local draft workspace** for a proposed repository to live under the `World-Semantic-Foundation` GitHub organisation.
> Proposed repo name: **`wsf-ecosystem`** (mirrors `wsf-connectors`, `wsf-visuals`, `wsf-examples`).
> Status of this workspace: **Candidate / Investigating** in WSF terms — content is being reconciled against the existing 27 ADRs before any ADR is raised.

---

## Purpose

This repository will provide a **complete, WSF-conformant semantic foundation for the Ecosystem domain**, including:

1. Three Tier 3 specialisations of foundational WSF concepts — **Ecosystem**, **Business Ecosystem**, **Digital Business Ecosystem** — plus a worked example in the spirit of `Capability`.
2. The **actor taxonomy** (Orchestrator, Complementor, Dominator, Gatekeeper, Prosumer, Boundary Spanner) as further Tier 3 specialisations.
3. **Architectural primitives** (Platform, Boundary Resources, Modularity, Interoperability Standards, Coupling Level).
4. **Value dynamics** (Network Effects with direct/indirect subtypes, Value Co-creation, Value Exchange, Value Slippage, Switching Costs, Lock-In).
5. **Governance mechanisms** (Decision Rights Allocation, Coopetition, Incentive Alignment, Trust Mechanisms).
6. **Lifecycle stages** (Birth, Expansion, Leadership, Self-Renewal/Death).
7. **Health metrics** (Productivity, Robustness, Niche Creation) decomposed per Iansiti & Levien.
8. **Relational properties** (the "verbs" — `orchestrates`, `complements`, `competes_with`, `cooperates_with`, `exhibits`, `provides`, `allocates_decision_rights_to`, `is_coupled_with`, `exchanges_value_with`, `co_creates_value_through`, `is_in_lifecycle_stage`, `measured_by`, `captures_value_from`, `slips_value_to`).
9. **Worked examples** drawn from the canonical `OTCHERE Inc` enterprise.

## How to read this workspace

| Path | What lives here |
|---|---|
| `proposals/` | The three top-level concept proposals (Ecosystem, Business Ecosystem, Digital Business Ecosystem) — one ADR-style proposal per concept |
| `concepts/tier-1/`, `tier-2/`, `tier-3/`, `worked-examples/` | Per-concept files using the ADR-WSF-20 §14 schema |
| `concepts/relationships/` | The relational properties file (the "verbs") |
| `concepts/metrics/`, `lifecycle/`, `governance/`, `health/` | Domain clusters that group concepts without re-tiering them |
| `research/` | Investigation findings — source reconciliation, tier classification, relationship grammar, modelling risks |
| `examples/` | Worked OTCHERE examples — the ecosystem, the platform/marketplace, the value flows |
| `governance/` | Tier-classification matrix, lifecycle diagrams, change-control trail |
| `diagrams/` | Mermaid sources for the concept maps and lifecycle diagrams |

## Tier-classification summary

See `governance/TIER-CLASSIFICATION-MATRIX.md` for the full reasoning per concept. Headline:

- **No concept in this repo is Tier 1.** Every domain concept can be derived from existing WSF Tier 1 primitives (Entity, Relationship, Event, State, Disposition, Proposition, Assertion, Context, Time, Space).
- **Tier 2 placeholders are limited to the constructs the existing vocabulary already elevates** (Identifier, Namespace, Term, Definition, Evidence, Provenance, Authority). The ecosystem repo does not propose new Tier 2 constructs.
- **Tier 3 is where almost everything lands**, with parent links to existing Tier 1 WSF primitives.
- **Worked example status** (in the sense of `Capability`) is reserved for **Ecosystem** itself — it is the demonstration that Tier 3 specialisation can ground a full domain ontology.

## Status and next steps

1. Reconcile this workspace against the four layered tier-validation checks documented in `research/02-tier-classification/`.
2. File the three top-level proposals under `proposals/` as `INV-FIND-WSF-28-Ecosystem.md` etc.
3. Draft the supporting ADRs (probably ADR-WSF-28 through ADR-WSF-31) for the actor taxonomy, value dynamics, governance, and lifecycle.
4. File a CR for each implementation step.
5. Once ratified upstream, mirror this workspace to `github.com/World-Semantic-Foundation/wsf-ecosystem`.

## Conventions

- All examples use **`OTCHERE Inc`** and the canonical individual **`Kwesi`** per the WSF Example Consistency Principle (ACME is prohibited).
- All concept files follow the **ADR-WSF-20 §14 metadata schema**.
- All tier assignments cite the validation check(s) used.
- All relational properties are **context-scoped** (platform, layer, time) per the Overlapping Roles principle.
