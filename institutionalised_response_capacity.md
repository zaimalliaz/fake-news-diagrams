
---

### `institutionalised_response_capacity.md`
```mermaid
flowchart LR
  %% Phase containers (manually arranged via subgraphs)

  subgraph Phase1[" "]
    direction TB
    SIT[Situation]
    AG[Agents]
    STR[Strategy]
    INT_SYS[Infrastructure Systems]
    INF_USERS[Infrastructure Users]
  end

  subgraph Phase2[" "]
    direction TB
    EVAL[Evaluation]
    INST_PRACT[Institutional Practices]
    LAW[Laws]
    ETH[Ethics]
    JUDG[Judgement]
    PER_AWR[Perception Awareness]
    PER_SENS[Perception Sensitivity]
  end

  subgraph Phase3[" "]
    direction TB
    MIT[Mitigation]
    IMP[Implementation]
    INTV[Intervention]
    THR[Intervention Thresholds]
    RSC[Resource Curtail]
  end

  %% Positioning via invisible nodes to match your layout
  Phase1 -->| | Phase2
  Phase1 -->| | Phase3
  Phase2 -->| | Phase3

  %% Phase 1 Connections
  AG --> INT_SYS
  SIT --> INT_SYS
  INT_SYS --> STR
  INT_SYS --> INF_USERS
  INF_USERS --> JUDG
  INF_USERS --> PER_AWR
  AG --> PER_AWR

  %% Phase 2 Connections
  STR --> INST_PRACT
  INT_SYS --> INST_PRACT
  EVAL --> INST_PRACT
  INST_PRACT --> LAW
  INST_PRACT --> ETH
  INST_PRACT --> PER_AWR
  ETH --> PER_SENS
  LAW --> PER_AWR
  PER_SENS --> PER_AWR
  PER_AWR --> JUDG

  %% Phase 3 Connections
  EVAL --> MIT
  PER_SENS --> THR
  ETH --> THR
  THR --> RSC
  MIT --> IMP
  IMP --> INTV
  INTV --> RSC

  %% Cross Phase Connections
  PER_AWR --> RSC

