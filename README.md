# Helm 3-Tier Application POC

## Objective

Deploy a secure 3-tier application using Helm on Kubernetes.

Components:

- Frontend
- Backend
- PostgreSQL

Features:

- Parent-child Helm architecture
- Helm hooks
- Network policies
- Ingress routing
- Secrets management
- Workload identity
- PVC for PostgreSQL

Helm 3-Tier Application POC
Objective
Deploy a secure 3-tier application using Helm on Kubernetes.

Components:

Frontend
Backend
PostgreSQL
Features:

Parent-child Helm architecture
Helm hooks
Network policies
Ingress routing
Secrets management
Workload identity
PVC for PostgreSQL

                    Internet
                        |
                        v
                NGINX Ingress
                      / \
                     /   \
                    /     \
                   v       v

            Frontend    Backend
                           |
                           |
                           v

                     PostgreSQL
                           |
                           v
                          PVC

Backend ---> Key Vault ---> Secrets

Backend ---> Workload Identity ---> Azure AD