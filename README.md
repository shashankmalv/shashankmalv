Shashank Malviya's DevOps Portfolio

🚀 About Me
I'm Shashank Malviya, a dedicated DevOps Engineer specializing in Development, DevOps, and Platform Engineering from 🇮🇳 India. With 3.5 years of professional experience in both onsite and remote environments, I focus on building production-ready applications and scalable cloud infrastructure. My passion lies in creating efficient, automated, and reliable DevOps pipelines.

🔭 Currently working on: Cloud-native solutions, AI-driven DevOps pipelines, and Platform Engineering.
🌱 Always learning: Emerging DevOps tools, cloud architectures, and best practices.
👯 Looking to collaborate on: Open-source DevOps projects and innovative cloud solutions.
💬 Ask me about: Python, Cloud Architecture, Kubernetes, CI/CD, and Platform Engineering.
⚡ Fun fact: I enjoy solving complex infrastructure challenges!

🛠️ Tech Stack
Languages & Frameworks
    
Cloud & DevOps
       
Databases & Monitoring
     
🏗️ DevOps Project Architecture
Below is the architecture diagram for my end-to-end DevOps pipeline, showcasing a modern workflow from code development to deployment and monitoring.
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
        I --> R[AppDynamics<br><img src="https://www.appdynamics.com/etc.clientlibs/appdynamics/clientlibs
