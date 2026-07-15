
# Cloud Native Microservices Platform

End-to-end deployment of a polyglot microservices application on AWS EKS using 
Terraform, Kubernetes, GitHub Actions, and ArgoCD with GitOps workflows.

## Architecture

> Architecture diagram will be added after infrastructure setup

## Tech Stack

| Layer | Tool |
|---|---|
| Cloud Provider | AWS (EKS, EC2, S3, ALB, Route53) |
| Infrastructure as Code | Terraform |
| Containerization | Docker |
| Orchestration | Kubernetes |
| CI Pipeline | GitHub Actions |
| CD / GitOps | ArgoCD |
| Container Registry | Amazon ECR |
| Monitoring | Prometheus + Grafana |

## Microservices

| Service | Language | Responsibility |
|---|---|---|
| Product Catalog | Golang | Manages product listings |
| Ad Service | Java | Serves targeted advertisements |
| Recommendation Service | Python | Suggests related products |
| Frontend | - | User interface |

## Project Structure

cloud-native-microservices-platform/
├── services/           # Microservice source code and Dockerfiles
├── infrastructure/     # Terraform modules (VPC, EKS, S3 backend)
├── kubernetes/         # K8s manifests (deployments, services, ingress)
├── .github/workflows/  # GitHub Actions CI pipelines
├── gitops/             # ArgoCD application definitions
├── monitoring/         # Prometheus and Grafana configuration
└── docs/               # Architecture diagrams and setup guides

## Key Design Decisions

**Why EKS over ECS?**
EKS gives full Kubernetes compatibility — portable across clouds and no vendor lock-in on the orchestration layer.

**Why ArgoCD for CD?**
Pull-based GitOps model — ArgoCD pulls desired state from Git rather than CI pushing to cluster. This means the cluster credentials never leave the cluster boundary.

**Why Terraform remote state with S3 + DynamoDB?**
Prevents state corruption when multiple engineers run terraform apply simultaneously. DynamoDB provides atomic locking.

**Why ALB Ingress over individual LoadBalancers?**
One ALB handles routing for all services — significantly cheaper than provisioning a LoadBalancer per service.

## Setup Guide

See [docs/setup-guide.md](docs/setup-guide.md)

## Progress

- [x] Environment setup (EC2, Docker, kubectl, Terraform)
- [ ] Microservice containerization
- [ ] Docker Compose local setup
- [ ] Terraform infrastructure provisioning
- [ ] EKS cluster deployment
- [ ] Kubernetes manifests
- [ ] CI pipeline with GitHub Actions
- [ ] GitOps with ArgoCD
- [ ] Monitoring with Prometheus + Grafana
