# 🚀 k8s-platform

Production-Ready Kubernetes Platform with GitOps, Infrastructure as Code, CI/CD, and Observability.

## 📌 Overview

k8s-platform is a cloud-native DevOps platform designed to simulate real-world production environments.  
It demonstrates modern platform engineering practices including GitOps deployments with ArgoCD, infrastructure provisioning with Terraform, application delivery with Helm, full observability with Prometheus and Grafana, CI/CD automation with GitHub Actions, and Kubernetes security best practices.

## 🧱 Architecture

Code is pushed to GitHub, CI/CD pipelines build and push Docker images, and GitOps (ArgoCD) continuously syncs the desired state to the Kubernetes cluster. The cluster runs applications, monitoring, and logging stacks in a fully automated way.

GitHub → GitHub Actions → Docker Registry → ArgoCD → Kubernetes Cluster

## 📁 Structure

- clusters/ → GitOps environments (dev, staging, prod)
- apps/ → Application manifests and Helm charts
- infrastructure/ → Terraform infrastructure code
- gitops/ → ArgoCD application definitions
- helm/ → Reusable Helm charts
- monitoring/ → Prometheus, Grafana, Alertmanager
- logging/ → Fluentbit and ELK stack
- ci-cd/ → CI/CD pipelines
- security/ → RBAC, network policies, pod security
- docs/ → Documentation and runbooks

## ⚙️ Tech Stack

Kubernetes, ArgoCD, Helm, Terraform, GitHub Actions, Prometheus, Grafana, Fluentbit, ELK, Nginx Ingress.

## 🚀 Getting Started

git clone https://github.com/hrmse/k8s-platform.git  
cd k8s-platform  

cd infrastructure/aws  
terraform init  
terraform apply  

kubectl create namespace argocd  
kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml  

kubectl apply -f gitops/argo-apps  

kubectl port-forward svc/argocd-server -n argocd 8080:443  

## 📊 Monitoring

Prometheus collects metrics from the cluster, Grafana visualizes dashboards, and Alertmanager handles alerts.

## 🔐 Security

RBAC, network policies, pod security standards, and secrets management are implemented for production-grade security.

## 🔄 CI/CD Flow

Code Push → GitHub Actions → Build Image → Push Registry → Update GitOps Repo → ArgoCD Sync → Kubernetes Deploy

## 🎯 Goal

This project is built to demonstrate real-world DevOps / Platform Engineering practices and production-grade Kubernetes architecture.

## 👨‍💻 Author

Built for learning, portfolio, and production-ready DevOps experience.
