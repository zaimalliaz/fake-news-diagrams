
```mermaid
graph TD
  subgraph Layer1["Data Collection & Awareness"]
    A1[Data Collection & Awareness]
  end

  subgraph Layer2["Risk Assessment & Strategy Formulation"]
    B1[Risk Assessment & Strategy Formulation]
  end

  subgraph Layer3["Detection & Classification"]
    C1[Detection & Classification]
  end

  subgraph Layer4["Verification & Fact Checking"]
    D1[Verification & Fact Checking]
  end

  subgraph Layer5["Enforcement & Mitigation"]
    E1[Enforcement & Mitigation]
  end

  %% Draw hierarchy bottom -> top
  A1 -->|Empowers| B1
  B1 -->|Facilitates| C1
  C1 -->|Determines| D1
  D1 -->|Enables| E1

  %% Add optional label for time variance (represented along layers)
  subgraph TimeVariance["Time Variance (across layers)"]
  end
