graph TD
    subgraph Git Repository [Git Source of Truth]
        A[C# & Scala Services Code]
        B[OpenAPI Specs / HTTP]
        C[AsyncAPI Specs / Kafka & RabbitMQ]
    end

    subgraph AI Testing Engine [AI Control Loop]
        D[AI Agent Engine]
        E[Dynamic Dependency Mapping]
    end

    subgraph AWS DevOps & EKS [Target Environment]
        F[AWS CodePipeline / CodeBuild]
        G[EKS Kubernetes Cluster]
        H[Kafka / RabbitMQ Event Streams]
    end

    %% Flow Lines
    A & B & C -->|1. Parse schemas & code deltas| D
    D -->|2. Generate internal test plan graph| E
    E -->|3. Generate programmatic assertions & triggers| F
    F -->|4. Deploy & execute test code| G
    G -->|5. Validate state & message queues| H
    G & H -->|6. Pipe test logs & metrics directly| D

    style D fill:#f9f,stroke:#333,stroke-width:2px
    style Git Repository fill:#e1f5fe,stroke:#0288d1
    style AWS DevOps & EKS fill:#efebe9,stroke:#5d4037
