# AWS Security Groups

## Purpose

Security Groups act as virtual firewalls for EC2 instances.

They control inbound and outbound network traffic.

---

## Ports Used

| Port | Purpose |
|------|----------|
| 22 | SSH Access |
| 8080 | Application |
| 9090 | Prometheus |
| 3000 | Grafana |

---

## Key Learnings

- Security Groups are stateful.
- Inbound rules define incoming traffic.
- Outbound rules define outgoing traffic.
- SSH access should be restricted whenever possible.