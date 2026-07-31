# Docker Compose

## Purpose

Docker Compose is used to run multiple containers using a single YAML configuration.

Instead of executing dozens of docker run commands, all services can be started with one command.

---

## Command Used

```bash
docker compose up -d
```

---

## Architecture

The application consists of multiple business services and supporting infrastructure.

Business Services

- Frontend
- Product Catalog
- Recommendation
- Checkout
- Cart
- Payment
- Shipping
- Currency
- Email
- Advertisement

Infrastructure Services

- PostgreSQL
- Kafka
- Valkey
- OpenSearch

Observability

- OpenTelemetry Collector
- Jaeger
- Prometheus
- Grafana

---

## Why Docker Compose?

- Local development
- Integration testing
- Multi-container orchestration
- Service networking

---

## Verification

All containers were successfully started using Docker Compose on an AWS EC2 instance.