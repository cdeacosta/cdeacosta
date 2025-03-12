```mermaid
graph LR
    A[IDE] --> B(Github);
    B --> C(Jenkins);
    C --> D[PyLint Style];
    subgraph E [Automated Tests]
        E1[Perf & Load Tests]
        E2[Smoke Tests]
    end
    C --> F{Build};
    F --> G[ECS Cluster QA];
    F --> H[ECS Cluster Perf];
    F --> I[ECS Cluster Staging];
    J[Static Code Analysis<br>Sonarcube] --> F;
    K[ECR] -.-> F;
    subgraph L [Monitoring]
        L1[Datadog]
        L2[CloudWatch]
        L3[AppDynamics]
    end
    H --> L;
    subgraph M [Monitoring]
        M1[Datadog]
        M2[CloudWatch]
        M3[AppDynamics]
    end
    I --> M;
    G --> E;
    H --> E;

    D --> R[Redis];
    E --> R;
    L --> R;
    M --> R;
    F --> R;

    R --> S[Redshift];
    S --> T[Power BI];

    C --> N[Slack<br>Build Started];
    F --> O[Slack<br>Build Completed];
    E --> P[Slack<br>Tests Completed];
    G --> Q[Slack<br>Deployed to QA];
    H --> R1[Slack<br>Deployed to Perf];
    I --> S1[Slack<br>Deployed to Staging];

    style N fill:#36C5F0,stroke:#fff,stroke-width:2px;
    style O fill:#36C5F0,stroke:#fff,stroke-width:2px;
    style P fill:#36C5F0,stroke:#fff,stroke-width:2px;
    style Q fill:#36C5F0,stroke:#fff,stroke-width:2px;
    style R1 fill:#36C5F0,stroke:#fff,stroke-width:2px;
    style S1 fill:#36C5F0,stroke:#fff,stroke-width:2px;
