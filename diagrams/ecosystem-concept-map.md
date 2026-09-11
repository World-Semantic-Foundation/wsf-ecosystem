# Ecosystem Concept Maps

Core Taxonomy & Actors (The "Who" and "What")

These are hree focused, thematic diagrams. This approach drastically reduces cognitive load by chunking the ontology into logical layers: Taxonomy & Actors, Structure & Value, and Lifecycle & Health.
 
## Source
> **This diagram establishes the foundational hierarchy and the entities that populate the ecosystem.**
```mermaid
graph TD
    subgraph T1["Tier 1: WSF Primitives"]
        SYS(("System"))
        ENT(("Entity"))
        ACT(("Actor"))
    end

    subgraph Tax["Domain Taxonomy"]
        ECO{"Ecosystem"}
        BE["Business Ecosystem"]
        DBE["Digital Business Ecosystem"]
    end

    subgraph Act["Ecosystem Actors"]
        ORCH["Orchestrator<br/>(Keystone)"]
        COMP["Complementor<br/>(Niche)"]
        DOM["Dominator<br/>(Degraded)"]
        GATE["Gatekeeper"]
        PROS["Prosumer"]
        BS["Boundary Spanner"]
    end

    %% Core Hierarchy
    SYS --> ECO
    ECO --> BE --> DBE

    %% Actor Specialisation
    ACT --> ORCH & COMP & GATE & PROS & BS
    ORCH -.->|degrades to| DOM

    %% Styling
    classDef tier1 fill:#f5f5f5,stroke:#616161,stroke-width:2px,color:#333
    classDef domain fill:#fff3e0,stroke:#ef6c00,stroke-width:3px,color:#333
    classDef actor fill:#e3f2fd,stroke:#1976d2,stroke-width:2px,color:#333

    class SYS,ENT,ACT tier1
    class ECO,BE,DBE domain
    class ORCH,COMP,DOM,GATE,PROS,BS actor
```

## Diagram 2: Structure, Governance & Value (The "How" and "Where")
This diagram maps the mechanics of the platform, how it is governed, and how value is created and captured.

```mermaid
graph LR
    subgraph T1["Tier 1 Primitives"]
        ENT(("Entity"))
        REL(("Relationship"))
        DISP(("Disposition"))
        PROP(("Proposition"))
        RULE(("Rule"))
        STA(("State"))
        EVT(("Event"))
    end

    subgraph Struct["Structure & Platform"]
        PLAT["Platform"]
        MKT["Marketplace"]
        BR["Boundary Resources"]
        MOD["Modularity"]
        IOS["Interoperability"]
        CPL["Coupling Level"]
    end

    subgraph Gov["Governance"]
        GOV["Governance"]
        DRA["Decision Rights"]
        COOP["Coopetition"]
        IA["Incentive Alignment"]
        TM["Trust"]
    end

    subgraph Val["Value Dynamics"]
        NE["Network Effects"]
        DNE["Direct NE"]
        INE["Indirect NE"]
        VCC["Value Co-creation"]
        VEX["Value Exchange"]
        VS["Value Slippage"]
        SWC["Switching Costs"]
        LOCK["Lock-In"]
    end

    %% Tier 1 Mappings
    ENT --> PLAT & BR
    DISP --> MOD & IA & SWC
    RULE --> IOS
    REL --> CPL & VEX & DRA
    PROP --> VCC & GOV
    STA --> COOP
    EVT --> VS

    %% Internal Flows
    PLAT --> MKT
    NE --> DNE & INE
    HEAL["Health"] ~~~| |Val %% Invisible link for alignment if needed
    
    %% Emergent/Compositional
    NE -.->|produces| LOCK
    SWC -.->|contributes to| LOCK
    COOP -.->|composes| GOV

    %% Styling
    classDef tier1 fill:#f5f5f5,stroke:#616161,stroke-width:2px,color:#333
    classDef struct fill:#e8f5e9,stroke:#388e3c,stroke-width:2px,color:#333
    classDef gov fill:#f3e5f5,stroke:#7b1fa2,stroke-width:2px,color:#333
    classDef val fill:#ffebee,stroke:#d32f2f,stroke-width:2px,color:#333

    class ENT,REL,DISP,PROP,RULE,STA,EVT tier1
    class PLAT,MKT,BR,MOD,IOS,CPL struct
    class GOV,DRA,COOP,IA,TM gov
    class NE,DNE,INE,VCC,VEX,VS,SWC,LOCK val
```

## Diagram 3: Lifecycle & Health (The "When" and "How Well")
This diagram focuses on temporal evolution and the metrics used to evaluate the system's viability.

```mermaid
graph TD
    subgraph T1["Tier 1 Primitives"]
        STA(("State"))
        DISP(("Disposition"))
        MES(("Measure"))
    end

    subgraph Eco["Ecosystem Context"]
        ECO{"Ecosystem"}
    end

    subgraph Life["Lifecycle Stages"]
        LC_B["Birth"]
        LC_E["Expansion"]
        LC_L["Leadership"]
        LC_R["Renewal / Death"]
    end

    subgraph Health["Health Metrics"]
        HEAL["Ecosystem Health"]
        PROD["Productivity"]
        ROB["Robustness"]
        NC["Niche Creation"]
    end

    %% Tier 1 Mappings
    STA --> LC_B & LC_E & LC_L & LC_R
    DISP --> HEAL
    MES --> PROD & ROB & NC

    %% Lifecycle flow
    LC_B --> LC_E --> LC_L --> LC_R

    %% Health decomposition
    HEAL -->|measured by| PROD & ROB & NC

    %% Emergent System States
    ECO -.->|state transition| LC_E
    ECO -.->|emergent property| HEAL
    ECO -.->|emergent property| LOCK["Lock-In<br/>(See Fig 2)"]

    %% Styling
    classDef tier1 fill:#f5f5f5,stroke:#616161,stroke-width:2px,color:#333
    classDef context fill:#fff3e0,stroke:#ef6c00,stroke-width:3px,color:#333
    classDef life fill:#fff9c4,stroke:#fbc02d,stroke-width:2px,color:#333
    classDef health fill:#e0f2f1,stroke:#00796b,stroke-width:2px,color:#333

    class STA,DISP,MES tier1
    class ECO context
    class LC_B,LC_E,LC_L,LC_R life
    class HEAL,PROD,ROB,NC health
```

> **Complete ecosystem domain concept map.** Reproducible per CR-WSF-17 Rev.1 §14.
```mermaid
graph LR
    %% Tier 1: Core Primitives (rounded nodes)
    subgraph T1["Tier 1: WSF Primitives"]
        direction TB
        SYS["System"]
        ENT["Entity"]
        ACT["Actor"]
        REL["Relationship"]
        STA["State"]
        EVT["Event"]
        DISP["Disposition"]
        PROP["Proposition"]
        RULE["Rule"]
        MES["Measure"]
    end

    %% Tier 2: Ecosystem Domain (diamond shape, central)
    ECO{"Ecosystem<br/>(Domain Concept)"}

    %% Tier 3: Consolidated into 4 semantic layers
    subgraph Social["Social Layer"]
        direction TB
        ORCH["Orchestrator<br/>(Keystone)"]
        COMP["Complementor<br/>(Niche)"]
        DOM["Dominator<br/>(degraded)"]
        GATE["Gatekeeper"]
        PROS["Prosumer"]
        BS["Boundary Spanner"]
        GOV["Governance"]
        DRA["Decision Rights"]
        COOP["Coopetition"]
        IA["Incentive Alignment"]
        TM["Trust"]
    end

    subgraph Economic["Economic Layer"]
        direction TB
        PLAT["Platform"]
        MKT["Marketplace"]
        BR["Boundary Resources"]
        MOD["Modularity"]
        IOS["Interoperability"]
        CPL["Coupling"]
        NE["Network Effects"]
        DNE["Direct NE"]
        INE["Indirect NE"]
        VCC["Value Co-creation"]
        VEX["Value Exchange"]
        VS["Value Slippage"]
        SWC["Switching Costs"]
        LOCK["Lock-In"]
    end

    subgraph Dynamic["Dynamic Layer"]
        direction TB
        LC_B["Birth"]
        LC_E["Expansion"]
        LC_L["Leadership"]
        LC_R["Renewal/Death"]
        HEAL["Health"]
        PROD["Productivity"]
        ROB["Robustness"]
        NC["Niche Creation"]
    end

    subgraph Taxonomy["Specialisations"]
        direction TB
        BE["Business Ecosystem"]
        DBE["Digital Business<br/>Ecosystem"]
    end

    %% Core relationships
    SYS --> ECO
    ECO --> BE --> DBE
    ACT --> ORCH & COMP & GATE & PROS & BS
    ORCH -.->|degrades to| DOM

    %% Tier 1 → Layer mappings
    ENT --> PLAT & BR
    DISP --> MOD & NE & IA & HEAL
    RULE --> IOS
    REL --> CPL & VEX & DRA
    PROP --> VCC & GOV
    EVT --> VS
    STA --> LOCK & COOP & LC_B & LC_E & LC_L & LC_R
    MES --> PROD & ROB & NC
    SYS --> TM

    %% Intra-layer relationships
    PLAT --> MKT
    NE --> DNE & INE
    NE -.->|produces| LOCK
    SWC -.->|contributes to| LOCK
    COOP -.->|composes| GOV
    HEAL -->|measured by| PROD & ROB & NC

    %% Styling
    classDef tier1 fill:#e1f5ff,stroke:#0288d1,stroke-width:2px
    classDef domain fill:#fff3e0,stroke:#f57c00,stroke-width:3px
    classDef social fill:#f3e5f5,stroke:#7b1fa2,stroke-width:2px
    classDef economic fill:#e8f5e9,stroke:#388e3c,stroke-width:2px
    classDef dynamic fill:#fff9c4,stroke:#f9a825,stroke-width:2px
    classDef taxonomy fill:#ffebee,stroke:#c62828,stroke-width:2px

    class SYS,ENT,ACT,REL,STA,EVT,DISP,PROP,RULE,MES tier1
    class ECO domain
    class ORCH,COMP,DOM,GATE,PROS,BS,GOV,DRA,COOP,IA,TM social
    class PLAT,MKT,BR,MOD,IOS,CPL,NE,DNE,INE,VCC,VEX,VS,SWC,LOCK economic
    class LC_B,LC_E,LC_L,LC_R,HEAL,PROD,ROB,NC dynamic
    class BE,DBE taxonomy
```


## Style note

This is the high-level concept map. Domain relationships (the 15 `wsf-rel-eco:*` predicates) are documented separately in `concepts/relationships/ecosystem-relational-properties.md` to keep this map readable.
