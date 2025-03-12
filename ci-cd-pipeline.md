```mermaid
graph LR
    A[IDE] --> B(Github);
    B --> C(Jenkins);
    C --> D[PyLint<br>Style];
    D --> E[Automated Tests<br>Perf & Load Tests<br>Smoke Tests];
    C --> F{Build};
    F --> G[ECS Cluster<br>QA];
    F --> H[ECS Cluster<br>Perf];
    F --> I[ECS Cluster<br>Staging];
    J[Static Code Analysis<br>Sonarcube] --> F;
    K[ECR] -.-> F;
    H --> L[1. Monitoring<br>• Datadog<br>• CloudWatch<br>• AppDynamics];
    I --> M[1. Monitoring<br>• Datadog<br>CloudWatch<br>• AppDynamics];
    G --> E;
    H --> E;
