graph LR
    A[RESTful API] --> B(Kafka Producer);
    B --> C(Kafka Broker);
    C --> D{Kafka Topics};

    D -- client_metrics --> E1(Kafka Client - client_metrics);
    D -- api_metrics --> E2(Kafka Client - api_metrics);
    D -- apm_data --> E3(Kafka Client - apm_data);
    D -- royalty_reporting --> E4(Kafka Client - royalty_reporting);

    E1 --> F1(S3 - client_metrics);
    E2 --> F2(S3 - api_metrics);
    E3 --> F3(S3 - apm_data);
    E4 --> F4(S3 - royalty_reporting);

    F1 --> G1(AWS Glue - client_metrics ETL);
    F2 --> G2(AWS Glue - api_metrics ETL);
    F3 --> G3(AWS Glue - apm_data ETL);
    F4 --> H(Teradata Parallel Transporter);

    G1 --> I1(Tableau - client_metrics Reporting);
    G2 --> I2(Tableau - api_metrics Reporting);
    G3 --> I3(Tableau - apm_data Reporting);
    H --> J[Teradata Database];

    J --> K[BI Team - Royalty Payments];

    subgraph Kafka Data Pipeline
        B;
        C;
        D;
        E1;
        E2;
        E3;
        E4;
    end

    subgraph S3 Storage
        F1;
        F2;
        F3;
        F4;
    end

    subgraph AWS Glue ETL
        G1;
        G2;
        G3;
    end

    subgraph Reporting
        I1;
        I2;
        I3;
        J;
        K;
    end

    style D fill:#f9f,stroke:#333,stroke-width:2px
    style C fill:#ccf,stroke:#333,stroke-width:2px
    style B fill:#cfc,stroke:#333,stroke-width:2px
    style A fill:#ffc,stroke:#333,stroke-width:2px
    style E1 fill:#fcc,stroke:#333,stroke-width:2px
    style E2 fill:#fcc,stroke:#333,stroke-width:2px
    style E3 fill:#fcc,stroke:#333,stroke-width:2px
    style E4 fill:#fcc,stroke:#333,stroke-width:2px
    style F1 fill:#efe,stroke:#333,stroke-width:2px
    style F2 fill:#efe,stroke:#333,stroke-width:2px
    style F3 fill:#efe,stroke:#333,stroke-width:2px
    style F4 fill:#efe,stroke:#333,stroke-width:2px
    style G1 fill:#efe,stroke:#333,stroke-width:2px
    style G2 fill:#efe,stroke:#333,stroke-width:2px
    style G3 fill:#efe,stroke:#333,stroke-width:2px
    style H fill:#efe,stroke:#333,stroke-width:2px
    style I1 fill:#efe,stroke:#333,stroke-width:2px
    style I2 fill:#efe,stroke:#333,stroke-width:2px
    style I3 fill:#efe,stroke:#333,stroke-width:2px
    style J fill:#efe,stroke:#333,stroke-width:2px
    style K fill:#efe,stroke:#333,stroke-width:2px
