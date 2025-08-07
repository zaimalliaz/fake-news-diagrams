# feedback_loops_thematic_alignment.md

```mermaid
---
config:
  layout: elk
  theme: dark
---

flowchart TB

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

    style A1 fill:#FFCDD2,stroke:#D50000
    style B1 fill:#BBDEFB,stroke:#2962FF
    style B2 fill:#BBDEFB,stroke:#2962FF
    style C1 stroke:#FF6D00,fill:#FFE0B2
    style C2 stroke:#FF6D00,fill:#FFE0B2
    style D1 stroke:none
    style FakeNewsSources stroke:none
    style Misinformation fill:#BBDEFB,stroke:#2962FF
    style Disinformation fill:#FFE0B2,stroke:#FF6D00
