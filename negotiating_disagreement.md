# Manifestation of Belief and Idea in Thought: How Disagreement is Negotiated

```mermaid
flowchart TB

%% ==============
%%  NODE STYLES
%% ==============
classDef articulation fill:#005F87,stroke:#003A5C,color:white,stroke-width:2px,font-family:Arial,font-size:14px,font-weight:bold
classDef ideas fill:#FFD43B,stroke:#CCAA00,color:#333,stroke-width:2px,font-family:Arial,font-size:14px
classDef belief fill:#5E4FA2,stroke:#4B3D84,color:white,stroke-width:2px,font-family:Arial,font-size:14px,font-weight:bold
classDef disagreement fill:#D62728,stroke:#A31F1F,color:white,stroke-width:2px,font-family:Arial,font-size:14px
classDef society fill:#F7F7F7,stroke:#D4D4D4,color:#333,stroke-width:1.5px,font-family:Arial,font-size:12px
classDef culture fill:#F7F7F7,stroke:#D4D4D4,color:#333,stroke-width:1.5px,font-family:Arial,font-size:12px

%% ==============
%%  NODES
%% ==============
A[Articulation]:::articulation
I[Ideas]:::ideas
B[Belief]:::belief
D[Disagreement]:::disagreement
S[Society]:::society
C[Culture]:::culture

%% ==============
%%  CONTEXT BOX
%% ==============
subgraph Context["Sociocultural Context"]
    S
    C
end
style Context fill:none,stroke:#999,stroke-width:1.5px,stroke-dasharray:5

%% ==============
%%  RELATIONSHIPS
%% ==============
A -->|Expresses| I
I -->|Transforms into| B
B -->|May challenge| D
D -->|Refines| B
D -->|Evolves| I
A -->|Communicates| B
I -->|Influences| S
I -->|Shapes| C
B -->|Impacts| C
B -->|Reinforces| C
S -->|Informs| I
C -->|Strengthens| B
I -.->|Manifests in| B
B -.->|Originates from| I

%% ==============
%%  LINE STYLES
%% ==============
linkStyle 0,1,2,3,4 stroke:#333,stroke-width:2px
linkStyle 5 stroke:#005F87,stroke-width:2px
linkStyle 6,7,8,9,10,11 stroke:#666,stroke-width:1.5px
linkStyle 12,13 stroke:#666,stroke-width:1.5px,stroke-dasharray:3
