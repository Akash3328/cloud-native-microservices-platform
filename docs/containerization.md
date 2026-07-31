# Containerization

## Overview

The application workload consists of multiple independent microservices written in different programming languages.

During this sprint, the services were containerized using Docker.

Containerization ensures that each service runs in an isolated and reproducible environment with all required dependencies bundled inside the image.

---

## Services Containerized

| Service | Language |
|----------|----------|
| Product Catalog | Go |
| Ad Service | Java |
| Recommendation | Python |

---

## Docker Build Lifecycle

1. Create Dockerfile
2. Build Docker Image
3. Run Container
4. Verify Application
5. Push Image to Registry

---

## Why Docker?

Docker solves the "works on my machine" problem.

Every developer, CI pipeline, and production server runs the exact same image.

---

## Multi-stage Builds

The Go and Java services use multi-stage builds.

Advantages:

- Smaller images
- Reduced attack surface
- Faster deployments
- Cleaner runtime image

---

## Layer Caching

Dependency files are copied before application source.

Benefits:

- Faster rebuilds
- Reduced network usage
- Better CI performance

---

## Container Registry

Container images are stored in a centralized registry.

During this project, images will later be pushed to Amazon ECR for Kubernetes deployments.

---

## Learning Outcomes

- Build Docker images
- Understand Docker layers
- Create optimized images
- Run multi-container applications