# Ecosystem Domain ADR Plan

> This file mirrors the ADR plan filed against `wsf-governance` and tracked in the GitHub Issues for this repository.

## Status

| Slot | Subject | ADR | Status | Depends on | GitHub Issue |
|---|---|---|---|---|---|
| Root | Ecosystem as Tier 3 Worked Example | ADR-WSF-28 | Proposed (PR open) | ADR-WSF-17, ADR-WSF-04, ADR-WSF-20, ADR-WSF-07 | #1 (closed) |
| Convention | Domain-Extension Numbering and Categorisation Convention | ADR-WSF-29 | Proposed (PR open) | ADR-WSF-17 | #2 (closed) |
| Domain ext. | Ecosystem Actor Taxonomy | ADR-WSF-30 | Awaiting ADR-WSF-28 Baseline | ADR-WSF-28 | #3 (open) |
| Domain ext. | Ecosystem Value Dynamics | ADR-WSF-31 | Awaiting ADR-WSF-30 Baseline | ADR-WSF-30 | #5 (open) |
| Domain ext. | Ecosystem Structural Primitives | ADR-WSF-32 | Awaiting ADR-WSF-30 Baseline | ADR-WSF-30 | #6 (open) |
| Domain ext. | Ecosystem Lifecycle and Health Metrics | ADR-WSF-33 | Awaiting ADR-WSF-30 and ADR-WSF-31 Baseline | ADR-WSF-30, ADR-WSF-31 | #7 (open) |
| Implementation | CR for wsf-spec integration | CR-WSF-28-Rev.1 | Awaiting ADR-WSF-28, -30, -31 Baseline | all of the above | #4 (open) |

## Filing sequence

1. ADR-WSF-28 reaches Baseline.
2. ADR-WSF-30 reaches Baseline.
3. ADR-WSF-31 reaches Baseline (parallel with ADR-WSF-32).
4. ADR-WSF-32 reaches Baseline (parallel with ADR-WSF-31).
5. ADR-WSF-33 reaches Baseline (depends on ADR-WSF-30 and ADR-WSF-31).
6. CR-WSF-28-Rev.1 filed; implements the registrations in `wsf-spec/`.

## Pull request

PR: https://github.com/World-Semantic-Foundation/wsf-governance/pull/1

## Convention reference

ADR-WSF-29 establishes the Domain-Extension Numbering and Categorisation Convention. The Ecosystem domain is the first user. Subsequent domain extensions follow the same scheme.

