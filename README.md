# infra-monitoring-stack

Production-grade monitoring stack built with Prometheus, Grafana, and Alertmanager — deployable via Docker Compose in minutes.

## Stack

| Component | Role |
|-----------|------|
| **Prometheus** | Metrics collection & storage |
| **Grafana** | Dashboards & visualization |
| **Alertmanager** | Alert routing & notifications |
| **Node Exporter** | Host-level metrics (CPU, RAM, disk, network) |

## Structure

```
infra-monitoring-stack/
├── docker-compose.yml
├── prometheus/
│   ├── prometheus.yml
│   └── alert.rules.yml
├── alertmanager/
│   └── alertmanager.yml
├── grafana/
│   └── provisioning/
│       ├── dashboards/
│       └── datasources/
└── docs/
    └── runbook-alerts.md
```

## Quick Start

```bash
git clone https://github.com/kaloyans/infra-monitoring-stack
cd infra-monitoring-stack
docker compose up -d
```

Then open:
- Grafana → http://localhost:3000 (admin / admin)
- Prometheus → http://localhost:9090
- Alertmanager → http://localhost:9093

## Alerts Included

- High CPU usage (> 85% for 5 minutes)
- High memory usage (> 90%)
- Disk space critical (> 85%)
- Instance down (no scrape for 1 minute)

## Requirements

- Docker
- Docker Compose v2+
