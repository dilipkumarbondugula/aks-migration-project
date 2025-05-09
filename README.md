# aks-migration-project

# AKS Migration Project

This project demonstrates the migration of on-prem workloads to AKS using Kubernetes, Helm, Terraform, and full CI/CD automation with Azure DevOps. Monitoring is integrated with Prometheus and Grafana, and networking is secured using Calico and Azure NSGs.

## Key Features
- IaC with Terraform (AKS, NSGs, VNet)
- Raw Kubernetes YAML + Helm chart migration
- Docker-based microservice
- Azure DevOps CI/CD Pipelines
- Prometheus & Grafana monitoring stack
- Secure NGINX Ingress setup with TLS
- Calico CNI-based network policy enforcement

## Getting Started
1. Provision AKS using Terraform
2. Build and push Docker image to ACR
3. Deploy using Helm via Azure Pipeline
4. Access the app via Ingress endpoint
5. Monitor metrics using Grafana dashboards
