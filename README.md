graph LR
    A[Developer Environment<br><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/vscode/vscode-original.svg" width="40" height="40"/> VS Code] -->|Code Push| B[GitHub<br><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/github/github-original.svg" width="40" height="40"/>]
    
    subgraph CI/CD Pipeline
        B --> C[GitHub Actions<br><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/github/github-original.svg" width="40" height="40"/>]
        B --> D[Jenkins<br><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/jenkins/jenkins-original.svg" width="40" height="40"/>]
        C -->|Build Docker Image| E[Docker<br><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/docker/docker-original.svg" width="40" height="40"/>]
        D -->|Build Docker Image| E
        E -->|Push Image| F[AWS ECR<br><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/amazonwebservices/amazonwebservices-original.svg" width="40" height="40"/>]
    end

    subgraph Deployment Stage
        F --> G[Helm<br><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/helm/helm-original.svg" width="40" height="40"/>]
        F --> H[ArgoCD<br><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/argocd/argocd-original.svg" width="40" height="40"/>]
        G --> I[AWS EKS<br><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/kubernetes/kubernetes-plain.svg" width="40" height="40"/>]
        H --> I
    end

    subgraph Infrastructure Layer
        I --> J[Pods]
        I --> K[Services]
        I --> L[Ingress]
        I --> M[AWS Load Balancer<br><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/amazonwebservices/amazonwebservices-original.svg" width="40" height="40"/>]
        M --> N[End Users]
    end

    subgraph Monitoring Layer
        I --> O[Prometheus<br><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/prometheus/prometheus-original.svg" width="40" height="40"/>]
        I --> P[Grafana<br><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/grafana/grafana-original.svg" width="40" height="40"/>]
        I --> Q[Splunk<br><img src="https://www.splunk.com/content/dam/splunk2/images/icons/icon-splunk.svg" width="40" height="40"/>]
        I --> R[AppDynamics<br><img src="https://www.appdynamics.com/etc.clientlibs/appdynamics/clientlibs/clientlib-site/resources/images/appd-logo.svg" width="40" height="40"/>]
        O --> S[Incident Response]
        P --> S
        Q --> S
        R --> S
    end

    style A fill:#f4f4f4,stroke:#0078d4,stroke-width:2px,color:#333
    style B fill:#f4f4f4,stroke:#4078c0,stroke-width:2px,color:#333
    style C fill:#f4f4f4,stroke:#4078c0,stroke-width:2px,color:#333
    style D fill:#f4f4f4,stroke:#d24939,stroke-width:2px,color:#333
    style E fill:#f4f4f4,stroke:#0db7ed,stroke-width:2px,color:#333
    style F fill:#f4f4f4,stroke:#ff9900,stroke-width:2px,color:#333
    style G fill:#f4f4f4,stroke:#00a4ef,stroke-width:2px,color:#333
    style H fill:#f4f4f4,stroke:#ff6a00,stroke-width:2px,color:#333
    style I fill:#f4f4f4,stroke:#326ce5,stroke-width:2px,color:#333
    style J fill:#f4f4f4,stroke:#326ce5,stroke-width:2px,color:#333
    style K fill:#f4f4f4,stroke:#326ce5,stroke-width:2px,color:#333
    style L fill:#f4f4f4,stroke:#326ce5,stroke-width:2px,color:#333
    style M fill:#f4f4f4,stroke:#ff9900,stroke-width:2px,color:#333
    style N fill:#f4f4f4,stroke:#333,stroke-width:2px,color:#333
    style O fill:#f4f4f4,stroke:#e6522c,stroke-width:2px,color:#333
    style P fill:#f4f4f4,stroke:#d83b01,stroke-width:2px,color:#333
    style Q fill:#f4f4f4,stroke:#00a1d6,stroke-width:2px,color:#333
    style R fill:#f4f4f4,stroke:#004d7f,stroke-width:2px,color:#333
    style S fill:#f4f4f4,stroke:#333,stroke-width:2px,color:#333
