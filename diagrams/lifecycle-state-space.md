# Lifecycle State-Space Diagram

> **Mermaid source for the ecosystem lifecycle state space.** Reproducible per CR-WSF-17 Rev.1 §14.

## Source

```mermaid
stateDiagram-v2
    [*] --> Birth

    Birth --> Expansion : Successful value-prop establishment
    Birth --> [*] : Failure (cold-start unresolved)

    Expansion --> Leadership : Network effects established, dominance achieved
    Expansion --> Birth : Major shock (regression)

    Leadership --> SelfRenewalOrDeath : Bifurcation point
    Leadership --> Expansion : Disruption (regain scale)

    state SelfRenewalOrDeath <<choice>>
    SelfRenewalOrDeath --> Birth : Successful renewal (new cycle)
    SelfRenewalOrDeath --> [*] : Failure (death)

    note right of Birth
        Cold-start problem.
        Value proposition crisp.
        Trajectory-setting governance.
    end note

    note right of Expansion
        Quality dilution risk.
        Infrastructure bottlenecks.
        Premature monetisation kills momentum.
    end note

    note right of Leadership
        Dominator drift risk.
        Bureaucratic ossification.
        Lock-in complacency.
    end note

    note right of SelfRenewalOrDeath
        Most consequential transition.
        Boundary Spanners + external sensing decisive.
    end note
```

## Modelling rules

1. States are **states** (specialisations of `wsf:State`), not a strictly linear path.
2. Transitions are **Events** that can be asserted with provenance.
3. Each state assertion MUST carry time validity.
4. Health, governance, and risk profiles differ per state — prescriptive analysis requires state context.
