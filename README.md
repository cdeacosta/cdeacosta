## Hi there 👋

<!--
**cdeacosta/cdeacosta** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.
# Welcome to My GitHub Profile

Hello! I'm glad you're here.

```mermaid
graph TD
    A[Transaction Sources (Trading, ATMs, Online)] --> B(Message Queue - Kafka/RabbitMQ);
    B --> C{End of Day?};
    C -- Yes --> D[Batch Processing (Spark/Hadoop)];
    C -- No --> A;
    D --> E[Data Validation & Transformation];
    E --> F[Risk Analysis (ML/Algorithms)];
    F --> G[Reporting & Auditing];
    G --> H[Data Warehouse (Snowflake/BigQuery)];
    D --> H;
