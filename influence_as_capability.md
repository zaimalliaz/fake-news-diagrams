# Influence as Capability

```mermaid
flowchart TD

  %% Group 1 – Monitoring & Correction
  subgraph MC [ " " ]
    A1[Monitoring]
    A2[Correction]
    A3[Update Rules]
  end

  %% Group 2 – Adaptation & Information
  subgraph AI [ " " ]
    B1[Adaptation]
    B2[Collective Information]
    B3[Defined Structures]
  end

  %% Group 3 – Processing & Dissemination
  subgraph PD [ " " ]
    C1[Processing Input]
    C2[Filter]
    C3[Verification]
    C4[Dissemination]
  end

  %% Connections
  A1 --> A2
  A2 --> A3
  A3 --> B1
  B1 --> B2
  B2 --> B3
  B3 --> C1
  C1 --> C2
  C2 --> C3
  C3 --> C4

  %% Style classes
  classDef group1Style fill:#e3f2fd,stroke:#2196f3,stroke-width:2px
  classDef group2Style fill:#e8f5e9,stroke:#4caf50,stroke-width:2px
  classDef group3Style fill:#fff3e0,stroke:#fb8c00,stroke-width:2px
  classDef subgraphStyle fill:#f9f9f9,stroke:#999,stroke-width:1px

  class A1,A2,A3 group1Style
  class B1,B2,B3 group2Style
  class C1,C2,C3,C4 group3Style

  class MC,AI,PD subgraphStyle


