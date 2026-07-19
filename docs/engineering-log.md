# Engineering Log

## Sprint 1 – Environment Setup

### Objective

Prepare a cloud-based development environment capable of running a cloud-native microservices application before provisioning Kubernetes infrastructure.

---

## Tasks Completed

- Created AWS Account
- Created IAM User with required permissions
- Launched Ubuntu EC2 Instance
- Connected to EC2 using SSH
- Installed Docker
- Installed Docker Compose
- Installed kubectl
- Installed Terraform
- Cloned the project repository
- Successfully started the application using Docker Compose

---

## Validation

Successfully executed:

```bash
docker compose up -d
```

Verified all application containers are running using:

```bash
docker ps
```

---

## Learnings

- Docker Compose allows multiple containers to be managed using a single configuration file.
- Every microservice runs independently inside its own container.
- Infrastructure preparation is essential before deploying applications to Kubernetes.
- EC2 acts as the remote DevOps workstation throughout the project.

---

## Challenges

No major issues encountered during environment setup.

---

## Next Sprint

Sprint 2 – Containerization of Individual Microservices