
---

### `institutionalised_response_capacity.md`
```mermaid
flowchart TD
  subgraph Phase1[Phase 1]
    SIT[Situation]
    STR[Strategy]
    AG[Agents]
    INFU[Infrastructure Users]
    INT[Intermediate Systems]
  end

  subgraph Phase2[Phase 2 - Evaluation]
    INP[Institutional Practices]
    LAW[Laws]
    ETH[Ethics]
    JUDG[Judgement]
    PR[Practices]
    RS[Resource Awareness]
    PS[Perception Sensitivity]
    INF[Influence]
  end

  subgraph Phase3[Phase 3 - Mitigation]
    MIT[Mitigation]
    IMP[Implementation]
    INTN[Intervention]
    INFO[Information Control / Governance]
    THR[Intervention Thresholds]
  end

  %% Connections
  AG --> INT
  INT --> STR
  STR --> INFU
  INFU --> INP
  INP --> LAW
  INP --> ETH
  ETH --> JUDG
  JUDG --> MIT
  MIT --> IMP
  IMP --> INTN
  INTN --> THR
  INFO --> IMP
