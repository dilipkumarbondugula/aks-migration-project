# aks-migration-project

# Project: On-Prem to Azure Kubernetes Service (AKS) Migration

This GitHub project contains a complete, production-ready codebase for migrating containerized workloads from on-premises to Azure Kubernetes Service (AKS). It includes infrastructure provisioning with Terraform, Kubernetes manifests transitioning to Helm charts, CI/CD automation using Azure DevOps, monitoring with Prometheus & Grafana, secure NGINX ingress setup, Calico network policies, and rollout strategies including blue-green deployments.

---

## Repository Structure
```text
aks-migration-project/
├── terraform/                  # Infrastructure as Code for Azure + AKS
│   ├── main.tf
│   ├── variables.tf
│   ├── outputs.tf
│   ├── provider.tf
│   └── backend.tf
├── manifests/                  # Raw Kubernetes YAML files
│   ├── deployment.yaml
│   ├── service.yaml
│   ├── ingress.yaml
│   └── configmap.yaml
├── helm-chart/                 # Helm chart for microservice deployment
│   ├── Chart.yaml
│   ├── values.yaml
│   └── templates/
│       ├── deployment.yaml
│       ├── service.yaml
│       ├── ingress.yaml
│       └── configmap.yaml
├── microservices/             # Sample microservice app
│   ├── app.py
│   ├── Dockerfile
│   └── requirements.txt
├── pipelines/                 # Azure DevOps YAML pipelines
│   ├── azure-pipelines.yml         # App pipeline
│   └── infra-pipeline.yml          # Infra pipeline
├── monitoring/                # Prometheus & Grafana setup
│   ├── prometheus-deployment.yaml
│   ├── grafana-deployment.yaml
│   └── dashboards/
│       └── sample-dashboard.json
├── ingress/                   # NGINX Ingress setup
│   ├── ingress-controller.yaml
│   └── tls-secret.yaml
├── scripts/                   # Automation scripts
│   ├── setup_kubeconfig.sh
│   ├── rollout_blue_green.sh
│   ├── deploy_crd.sh
│   └── check_network_policies.sh
└── README.md

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
