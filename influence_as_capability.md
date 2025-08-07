# Influence as Capability

```mermaid
flowchart TD

  subgraph Box1["Monitoring & Correction"]
    A1[Monitoring]
    A2[Correction]
    A3[Update Rules]
  end

  subgraph Box2["Adaptation & Information"]
    B1[Adaptation]
    B2[Collective Information]
    B3[Defined Structures]
  end

  subgraph Box3["Processing & Dissemination"]
    C1[Processing Input]
    C2[Filter]
    C3[Verification]
    C4[Dissemination]
  end

  A1 --> A2
  A2 --> A3
  A3 --> B1
  B1 --> B2
  B2 --> B3
  B3 --> C1
  C1 --> C2
  C2 --> C3
  C3 --> C4
