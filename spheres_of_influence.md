# 🌐 Spheres of Influence Diagram

This Mermaid diagram illustrates the flow of global to local influence in policy and detection systems.

```mermaid
flowchart TD

  %% Macro-Level
  subgraph Macro-Level Components
    SF[Standard Framework]
    AM[Activity Model]
    ID[Interface Description]
    SP[Standard Profile]
  end

  SF -->|Defines| SP
  AM -->|Updates| RC

  %% Socio-Level
  subgraph Socio-Level Components
    RC[Relationship Chart]
    AM2[Activity Model]
    TM[Translation Matrix]
  end

  AM -->|Drives| RC
  RC --> AM2
  RC -->|Validates| TM
  AM2 -->|Maps To| TM

  %% Micro-Level
  subgraph Micro-Level Components
    ET[Event Trace]
    FD[Functionality Description]
    PM[Policy Model]
    RF[Resource Flow]
  end

  SP -->|Guides| RF
  ID -->|Controls| RF
  ET -->|Informs| RF
  TM -->|Refines| FD

 
  classDef macro fill:#1f77b4,color:#fff,stroke:#333,stroke-width:1px;   
  classDef socio fill:#2ca02c,color:#fff,stroke:#333,stroke-width:1px;   
  classDef micro fill:#d62728,color:#fff,stroke:#333,stroke-width:1px;   

  
  class SF,AM,ID,SP macro;
  class RC,AM2,TM socio;
  class ET,FD,PM,RF micro;
