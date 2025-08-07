# feedback_loops_thematic_alignment.md

```mermaid
---
config:
  layout: elk
  theme: dark
---

flowchart TB

  %%FakeNewsSource-level
 subgraph FakeNewsSources["Fake News Sources"]
        A1[/"Social Media
          Cross-Border Collaboration
          Global Monitoring"/]
  end

 subgraph Misinformation["Misinformation
      _Shared Without Intent to Harm_"]
        B1["• Public Awareness
          • Corrective Action"]
        B2["• Confusion
          • Fact Distortion"]
  end

 subgraph Disinformation["Disinformation
    _Deliberately Create to Deceive_"]
        C1["• Opinion Sway
          • Financial Gain"]
        C2["• Societal Harm
          • Community Division"]
  end

 subgraph Feedback["**Feedback Loop**"]
        D1["• Reinforces False Claims
          • Increases Spread"]
  end

 FakeNewsSources -- Leads to --> Misinformation
 Misinformation -- Creates Confusion --> Feedback
 Misinformation <-- Enables More --> Feedback
Disinformation -- Appears Credible --> Feedback
 Misinformation <-- Reinforces --> Disinformation
FakeNewsSources -- Leads to --> Disinformation
 Feedback -- Facilitates --> Disinformation

  classDef Red fill:#d62728,color:#fff,stroke:#333,stroke-width:1px;
  classDef Blue fill:#1f77b4,color:#fff,stroke:#333,stroke-width:1px;   
  classDef Orange fill:#ff7f50,color:#fff,stroke:#333,stroke-width:1px;   

  class A1 Red;
  class B1,B2,Misinformation Blue;
  class C1,C2,Disinformation Orange;
  
