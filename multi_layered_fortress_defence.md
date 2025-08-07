```mermaid
flowchart LR
 subgraph Governance["Governance Layer"]
        CP["Capability Phasing"]
  end
 subgraph Implementation["Implementation Layer"]
        CA["Capability Activities"]
        CD["Capability Development"]
  end
 subgraph Strategic["Strategic Layer"]
        V["Vision"]
  end
 subgraph Core["Core Components"]
        T["Taxonomy"]
        D["Dependencies"]
        C["Concepts"]
  end
    CP -- Influences --> CA & CD
    V -- Informs --> T
    T -- Informs --> D
    D -- Informs --> C
    T --> CA
    C --> CD
    PR["Portfolio Relationships"] -- Guides --> CA
    PM["Project to Capability Mapping"] -- Guides --> CD
    CP --> PR
    PM --> C

     CP:::governanceStyle
     CA:::implementationStyle
     CD:::implementationStyle
     V:::strategicStyle
     T:::coreStyle
     D:::coreStyle
     C:::coreStyle
     PR:::mapStyle
     PM:::mapStyle
    classDef governanceStyle fill:#ffcc80,stroke:#f57c00,stroke-width:2px
    classDef implementationStyle fill:#a5d6a7,stroke:#388e3c,stroke-width:2px
    classDef strategicStyle fill:#81d4fa,stroke:#0277bd,stroke-width:2px
    classDef coreStyle fill:#b39ddb,stroke:#4527a0,stroke-width:2px
    classDef mapStyle fill:#80cbc4,stroke:#00695c,stroke-width:2px
    classDef groupStyle fill:#f5f5f5,stroke:#9e9e9e,stroke-width:1px
