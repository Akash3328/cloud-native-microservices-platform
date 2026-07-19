# Development Environment

## Local Machine

| Component | Value |
|-----------|-------|
| Operating System | Windows |
| IDE | Visual Studio Code |
| Terminal | PowerShell |
| Version Control | Git |

---

## Remote Development Machine

| Component | Value |
|-----------|-------|
| Cloud Provider | AWS |
| Service | EC2 |
| Operating System | Ubuntu |
| Purpose | Remote DevOps Workstation |

---

## Installed Tools

- Docker
- Docker Compose
- kubectl
- Terraform
- Git

---

## Verification Commands

```bash
docker --version

docker compose version

kubectl version --client

terraform version

git --version
```

---

## Purpose

This EC2 instance is used as the primary development environment for:

- Building container images
- Running Docker Compose
- Provisioning AWS infrastructure
- Managing Kubernetes clusters
- Executing Terraform commands