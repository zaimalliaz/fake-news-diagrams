# Influence as Capability

```mermaid
flowchart TD

  %% Group 1: Monitoring & Correction
  subgraph Group1[Monitoring & Correction]
    A1[Monitoring]
    A2[Correction]
    A3[Update Rules]
  end

  %% Group 2: Adaptation & Information
  subgraph Group2[Adaptation & Information]
    B1[Adaptation]
    B2[Collective Information]
    B3[Defined Structures]
  end

  %% Group 3: Processing & Dissemination
  subgraph Group3[Processing & Dissemination]
    C1[Processing Input]
    C2[Filter]
    C3[Verification]
    C4[Dissemination]
  end

  %% Flow
  A1 --> A2
  A2 --> A3
  A3 --> B1
  B1 --> B2
  B2 --> B3
  B3 --> C1
  C1 --> C2
  C2 --> C3
  C3 --> C4


