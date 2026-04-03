# Tools

A collection of development tools and services configured via Docker Compose.

## Contents

| Directory | Description |
|-----------|-------------|
| [Kafka/](#kafka) | Event streaming platform with web UI |
| [Mlflow/](#mlflow) | ML experiment tracking and model registry |
| [Prometheus & Grafana/](#prometheus--grafana) | Metrics monitoring and visualization |
| [Redis/](#redis) | In-memory cache/database with GUI |

---

### Kafka

Event streaming platform for building real-time data pipelines.

**Files:**
- `docker-compose.yml` - Kafka cluster configuration
- `README.md` - Setup and usage instructions

**Services:**
- **Kafka** - Message broker (apache/kafka:latest)
- **AKHQ** - Kafka web UI (tchiotludo/akhq:latest)

**Access:** http://localhost:8080/ui/docker-kafka-server/topic

---

### Mlflow

Machine learning experiment tracking, model registry, and reproducibility platform.

**Files:**
- `docker-compose.yaml` - MLflow stack configuration
- `README.md` - Setup and usage instructions
- `.env` - Environment variables

**Services:**
- **PostgreSQL** - Metadata store (port 5432)
- **RustFS** - S3-compatible artifact storage (port 9000)
- **MLflow** - Tracking server UI (port 8080)

---

### Prometheus & Grafana

Full monitoring stack for metrics collection and visualization.

**Files:**
- `docker-compose.yml` - Stack configuration
- `prometheus.yml` - Prometheus scrape configuration
- `grafana/provisioning/datasources/datasources.yml` - Grafana datasource setup

**Services:**
- **Prometheus** - Metrics collection (port 9090)
- **Grafana** - Visualization dashboard (port 3000)

**Default credentials:** admin/admin

---

### Redis

In-memory data store with optional web-based management UI.

**Files:**
- `docker-compose.yml` - Redis configuration
- `README.md` - Setup and usage instructions

**Services:**
- **Redis** - In-memory database (port 6379) with AOF persistence
- **RedisInsight** - Browser-based Redis GUI (port 5540)
