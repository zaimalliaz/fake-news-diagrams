# 🌐 Spheres of Influence Diagram

This Mermaid diagram illustrates the flow of global to local influence in policy and detection systems.

```mermaid
flowchart TD

  %% Top-Level Elements (Key Relationships)
  ST[State Transitions]
  ET[Event Traces]
  RM[Resource Matrices]
  TM[Traceability Matrix]
  FE[Forecast Evolution]

  %% Mid-Level Element (Core Context)
  MLC[Macro-Level Context]

  %% Bottom-Level Elements (Core Components)
  FR[Functionality Requirements]
  CAP[Capabilities]
  OS[Operational Scenarios]

  %% Grouping (optional, visual clarity)
  subgraph Top-Level Elements
    ST
    ET
    RM
    TM
    FE
  end

  subgraph Core Components
    FR
    CAP
    OS
  end

  %% Relationships
  ST -->|Defines| MLC
  ET -->|Informs| MLC
  RM -->|Supports| MLC
  MLC -->|Influences| FR
  MLC -->|Context for| CAP
  TM -->|Maps to| CAP
  FE -->|Guides| CAP
  CAP -->|Enables| OS
