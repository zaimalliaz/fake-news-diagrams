# Spheres of Influence

```mermaid
flowchart TD
    %% Global Components (Top Layer)
    subgraph Global [" "]
        A1[International Standards]
        A2[Cross-Border Collaboration] 
        A3[Global Monitoring]
    end
    
    %% Regional Components (Middle Layer)  
    subgraph Regional [" "]
        B1[Regional Regulations]
        B2[Localised Detection]
        B3[Cultural Context]
    end
    
    %% Local Components (Bottom Layer)
    subgraph Local [" "]
        C1[Community Networks] 
        C2[Direct Verification]
        C3[Immediate Response]
    end
    
    %% Only vertical connections (no horizontal circles)
    A1 -.->|Standards<br/>Enforcement| B1
    A2 -.->|Collaboration<br/>Framework| B2  
    A3 -.->|Monitoring<br/>Data| B3
    
    B1 -.->|Regulation<br/>Implementation| C1
    B2 -.->|Detection<br/>Methods| C2
    B3 -.->|Context<br/>Adaptations| C3
    
    %% Styling for rectangular layout
    classDef globalStyle fill:#e1f5fe,stroke:#01579b,stroke-width:2px
    classDef regionalStyle fill:#e8f5e8,stroke:#2e7d32,stroke-width:2px  
    classDef localStyle fill:#fff3e0,stroke:#ef6c00,stroke-width:2px
    classDef subgraphStyle fill:#f8f9fa,stroke:#6c757d,stroke-width:1px
    
    class A1,A2,A3 globalStyle
    class B1,B2,B3 regionalStyle
    class C1,C2,C3 localStyle
    class Global,Regional,Local subgraphStyle
