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
  AM -->|Updates| SP
  ID -->|Controls| RF[Resource Flow]

  %% Socio-Level
  subgraph Socio-Level Components
    RC[Relationship Chain]
    AM2[Activity Model]
    TM[Translation Matrix]
  end

  AM -->|Drives| RC
  RC <--> AM2
  RC -->|Validates| TM
  AM2 -->|Maps To| TM

  %% Micro-Level
  subgraph Micro-Level Components
    ET[Event Trace]
    FD[Functionality Description]
    PM[Policy Model]
  end

  SP -->|Guides| RF
  ET -->|Informs| FD
  FD -->|Refines| PM

  %% Other Connections
  SP -->|Guides| ET
