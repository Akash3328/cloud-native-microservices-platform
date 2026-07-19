# Running Services

The application is composed of multiple independent containers.

## Core Business Services

| Service | Responsibility |
|----------|----------------|
| Frontend | User Interface |
| Frontend Proxy | Reverse Proxy |
| Product Catalog | Product Information |
| Recommendation | Product Recommendations |
| Cart | Shopping Cart |
| Checkout | Checkout Workflow |
| Payment | Payment Processing |
| Shipping | Shipping Service |
| Currency | Currency Conversion |
| Email | Email Notifications |
| Advertisement | Advertisement Engine |

---

## Infrastructure Services

| Service | Responsibility |
|----------|----------------|
| PostgreSQL | Database |
| Kafka | Event Streaming |
| Valkey | In-memory Cache |
| OpenSearch | Search Engine |

---

## Observability Stack

| Service | Responsibility |
|----------|----------------|
| OpenTelemetry Collector | Collects Telemetry |
| Jaeger | Distributed Tracing |
| Prometheus | Metrics Collection |
| Grafana | Dashboards |

---

## Feature Flags

- Flagd
- Flagd UI

---

## Load Testing

Load Generator continuously generates application traffic for testing and observability.