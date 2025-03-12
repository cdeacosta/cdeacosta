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
    S --> T[Data Analysis];
