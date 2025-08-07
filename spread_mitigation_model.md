
```mermaid

flowchart TD
    %% Top layer
    A["Enforcement & Mitigation"]
    %% Layer 4
    B["Verification & Fact Checking"]
    %% Layer 3
    C["Detection & Classification"]
    %% Layer 2
    D["Risk Assessment & Strategy Formulation"]
    %% Bottom layer (base of the pyramid)
    E["Data Collection & Awareness"]
    
    %% Connections top to bottom
    A -->|Enables| B
    B -->|Determines| C
    C -->|Facilitates| D
    D -->|Empowered by| E
    
    %% Time Variance positioned separately
    TV["Time Variance"]
