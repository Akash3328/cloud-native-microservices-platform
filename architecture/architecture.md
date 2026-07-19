# Project Architecture

## Overview

This project follows a cloud-native microservices architecture.

Instead of building one large application (Monolith), every business capability is implemented as an independent microservice.

Each service runs inside its own Docker container and communicates over the network.

During local development, Docker Compose manages all services.

In later stages, Docker Compose will be replaced by Kubernetes running on AWS Elastic Kubernetes Service (EKS).

---

## Major Components

Application Services

- Frontend
- Frontend Proxy
- Product Catalog
- Recommendation
- Checkout
- Cart
- Payment
- Shipping
- Currency
- Email
- Quote
- Advertisement
- Accounting
- Fraud Detection
- Image Provider

Supporting Services

- PostgreSQL
- Valkey (Redis compatible)
- Kafka
- OpenSearch

Observability

- OpenTelemetry Collector
- Jaeger
- Prometheus
- Grafana

Feature Management

- Flagd
- Flagd UI

Load Testing

- Load Generator

---

## Architecture Style

Cloud Native

Microservices

Containerized

Event Driven

Observability Enabled

GitOps Ready