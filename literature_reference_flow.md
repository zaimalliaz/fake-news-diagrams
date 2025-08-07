```mermaid
flowchart LR

  %% === Inputs ===
  AT[Abstraction/Theory]
  EC[Ethical Concepts]
  CB[Context/Background]
  WV[Worldviews/Paradigms]
  LR[Literature Review]
  WS[Western Sources]
  CF[Cultural Frameworks]
  EQ[Epistemological Questions]

  %% === Research Activities ===
  GR[Group Framing]
  PR[Project Rationale]
  RS[Research Strategy]
  DC[Data Collection]
  DA[Data Analysis]
  INT[Interpretation]

  %% === Outputs ===
  RC[Research Contribution]
  AC[Academic Conversation]
  KT[Knowledge Translation]

  %% === Inputs to Literature Review & Framing ===
  AT --> LR
  EC --> LR
  CB --> LR
  WV --> LR
  EQ --> LR

  LR --> GR
  LR --> PR
  CF --> GR
  WS --> PR
  EQ --> PR

  %% === Framing to Research Activity ===
  GR --> RS
  PR --> RS
  RS --> DC
  DC --> DA
  DA --> INT

  %% === Interpretation to Outcomes ===
  INT --> RC
  INT --> AC
  INT --> KT

  %% === Styling ===
  classDef inputStyle fill:#b2dfdb,stroke:#00695c,stroke-width:2px
  classDef processStyle fill:#d1c4e9,stroke:#512da8,stroke-width:2px
  classDef outputStyle fill:#bbdefb,stroke:#0d47a1,stroke-width:2px

  class AT,EC,CB,WV,EQ,WS,CF,LR inputStyle
  class GR,PR,RS,DC,DA,INT processStyle
  class RC,AC,KT outputStyle

  classDef outputStyle fill:#bbdefb,stroke:#0d47a1,stroke-width:2px

  class AT,EC,CB,WV,EQ,WS,CF,LR inputStyle
  class GR,PR,RS,DC,DA,INT processStyle
  class RC,AC,KT outputStyle
