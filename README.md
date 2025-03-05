![Chris DeAcosta](ChrisDeAcostaCard.png)

Hi there 👋 I'm Chris DeAcosta
I'm glad you're here.
Welcome to My GitHub Profile

---

High Level real world application I've just completed for a client.

```mermaid
graph LR
    A[Transaction Sources] --> B(Message Queue - Kafka/AWS-MSK/Azure-Events-Hub);
    B --> C{End of Day?};
    C -- Yes --> D["Batch Processing (Spark/Hadoop)"];
    C -- No --> A;
    D --> E[Data Validation & Transformation];
    E --> F["Risk Analysis (ML/Algorithms)"];
    F --> G[Reporting & Auditing];
    G --> H["Data Warehouse (Snowflake/BigQuery)"];
    D --> H;
```

---

```mermaid
graph LR
    A[IoT Devices (MQTT)] --> B(AWS IoT Core);
    B --> C(DataStax Astra Streaming);
    C --> D(DataStax Astra DB);
    D --> E(AWS API Gateway);
    E --> F[Microservices];
```

---

```

- 🔭 I’m currently working on ... Data Pipelines in AWS using IoT telemetry data --> IoT Core --> Astra Streaming --> Astra DB
- 🌱 I’m currently learning ... FinOps Cloud Practitioner (Nearly done with Course) FinOps Foundation is Awesome!!!
- 👯 I’m looking to collaborate on ... FinOps tasks
- 💬 Ask me about ... Data Pipelines
- 📫 How to reach me: ... chris.deacosta@gmail.com
- ⚡ Fun fact: ... I love bass fishing, and looking for that elusive lunker bass. -->
```
