# Tools

A collection of development tools and services configured via Docker Compose.

## Contents

| Directory | Description |
|-----------|-------------|
| [Kafka/](#kafka) | Event streaming platform with web UI |
| [Mlflow/](#mlflow) | ML experiment tracking and model registry |
| [Prometheus & Grafana/](#prometheus--grafana) | Metrics monitoring and visualization |
| [Redis/](#redis) | In-memory cache/database with GUI |
| [ElasticSearch/](#elasticsearch) | Under construction |
| [Langfuse/](#langfuse) | LLM observability and analytics |
| [Mongo/](#mongo) | Under construction |
| [Opensearch/](#opensearch) | Under construction |
| [Postgres/](#postgres) | Under construction |
| [RabbitMQ/](#rabbitmq) | Under construction |
| [RustFS/](#rustfs) | Under construction |

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

---

### Langfuse

LLM observability platform for tracing, evaluation, and analytics.

**Files:**
- `docker-compose.yml` - Langfuse stack configuration
- `README.md` - Setup and usage instructions

**Services:**
- **Langfuse** - Web UI (port 3000)
- **PostgreSQL** - Primary database (port 5432)
- **ClickHouse** - Analytics database (ports 8123, 9000)
- **Redis** - Caching and queue (port 6379)
- **MinIO** - S3-compatible storage (port 9090)

**Access:** http://localhost:3000


