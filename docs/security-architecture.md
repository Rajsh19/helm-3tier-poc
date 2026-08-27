# Three Tier Application Architecture

## Components

- Frontend (Nginx)
- Backend (NodeJS)
- PostgreSQL

## Kubernetes Resources

- Deployment
- Service
- PVC
- Ingress
- NetworkPolicy
- Secret
- ServiceAccount
- Helm Hook Job

## Secret Management Flow

Azure Key Vault
        |
External Secrets Operator
        |
Kubernetes Secret
        |
Backend / PostgreSQL Pods

## Workload Identity

Backend Pod
      |
ServiceAccount
      |
Azure Workload Identity
      |
Azure Key Vault

## CI/CD Flow

Developer
    |
GitHub Repository
    |
GitHub Actions
    |
helm lint
helm template
    |
Kubernetes Cluster