```mermaid

graph TD
    A [Situation: Pressure to Produce Reports] --> B{Task: Design Data Pipeline};
    B --> C[Action: Data Ingestion & Storage];
    C --> D[CUR Data: S3 Bucket];
    D --> E[AWS Glue (CUR): Process & Transform];
    E --> F[Redshift: CUR Data Storage];
    C --> G[CloudWatch Metrics: Metric Streams];
    G --> H[Kinesis Data Firehose: Centralized Stream];
    H --> I[S3: CloudWatch Metrics Storage];
    I --> J[AWS Glue (CloudWatch): Process & Transform];
    J --> F;
    F --> K[Action: Data Transformation & Merging];
    K --> L[AWS Glue (PySpark): Transformation & Joins];
    L --> M{Normalization & Standardization};
    M --> N{Join CUR & CloudWatch Data};
    N --> O{Calculated Fields (Idle, Volumes, etc.)};
    O --> P{Untagged Assets Logic};
    P --> Q[Action: Data Warehousing (Redshift)];
    Q --> R{Store Merged & Transformed Data};
    R --> S{Create Tables & Views};
    S --> T{Partition & Index};
    T --> U[Action: Reporting & Analysis];
    U --> V[Power BI: Dashboards & Reports];
    V --> W{Interactive Dashboards};
    U --> X[SQL Queries: Ad-hoc Analysis];
    X --> Y[Action: Automation & Orchestration];
    Y --> Z[AWS Step Functions: Pipeline Orchestration];
    Z --> AA{Reliable & Automatic Pipeline};
    Y --> AB[CloudWatch Events (EventBridge): Trigger Workflow];
    AB --> AC{Scheduled/Event-Based Trigger};
    AC --> AD[Result: 20% Cost Reduction in 3 Months];
    AD --> AE{Improved Visibility};
    AE --> AF{Impressed CFO & Finance};
    
    subgraph Data Ingestion and Storage
        D;E;F;G;H;I;J;
    end
    
    subgraph Data Transformation and Merging
        K;L;M;N;O;P;
    end
    
    subgraph Data Warehousing
        Q;R;S;T;
    end
    
    subgraph Reporting and Analysis
        U;V;W;X;
    end
    
    subgraph Automation and Orchestration
        Y;Z;AA;AB;AC;
    end

```
