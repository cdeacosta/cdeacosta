Hi there 👋 I'm Chris DeAcosta
I'm glad you're here.
Welcome to My GitHub Profile

```mermaid
graph TD
    A[Transaction Sources] --> B(Message Queue - Kafka/RabbitMQ);
    B --> C{End of Day?};
    C -- Yes --> D["Batch Processing (Spark/Hadoop)"];
    C -- No --> A;
    D --> E[Data Validation & Transformation];
    E --> F["Risk Analysis (ML/Algorithms)"];
    F --> G[Reporting & Auditing];
    G --> H["Data Warehouse (Snowflake/BigQuery)"];
    D --> H;
