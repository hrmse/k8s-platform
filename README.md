# k8s-platform
Production-Ready Kubernetes Platform with GitOps, Monitoring and CI/CD




                GitHub
                   │
         ┌─────────┴─────────┐
         │                   │
   CI/CD (Actions)     GitOps Repo
         │                   │
     Docker Image        ArgoCD
         │                   │
         └─────────┬─────────┘
                   Kubernetes
     ┌─────────────┼─────────────┐
     │             │             │
  App Pods    Monitoring     Logging
 (Helm)      (Prometheus)   (ELK/Fluent)
