# Tools

A collection of development tools and services configured via Docker Compose.

## Contents

| Directory | Description |
|-----------|-------------|
| [Cassandra/](#cassandra) | NoSQL distributed database |
| [Kafka/](#kafka) | Event streaming platform with web UI |
| [Mlflow/](#mlflow) | ML experiment tracking and model registry |
| [Mongo/](#mongodb) | Document database |
| [Neo4j/](#neo4j) | Graph database |
| [Postgres/](#postgres) | Relational database |
| [Prometheus & Grafana/](#prometheus--grafana) | Metrics monitoring and visualization |
| [RabbitMQ/](#rabbitmq) | Message broker |
| [Redis/](#redis) | In-memory cache/database with GUI |
| [RustFS/](#rustfs) | S3-compatible object storage |
| [Langfuse/](#langfuse) | LLM observability and analytics |
| [Consul/](#consul) | Under construction |
| [Eureka/](#eureka) | Under construction |
| [Infisical/](#infisical) | Under construction |
| [Spark/](#spark) | Under construction |
| [Vault/](#vault) | Under construction |
| [Zookeeper/](#zookeeper) | Under construction |

---

### Cassandra

NoSQL distributed database designed to handle large amounts of data across commodity servers.

**Files:**
- `docker-compose.yml` - Cassandra cluster configuration
- `README.md` - Setup and usage instructions

**Services:**
- **Cassandra** - NoSQL database (port 9042)

**Connection:** `localhost:9042`

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

### MongoDB

Document database for modern applications.

**Files:**
- `docker-compose.yml` - MongoDB configuration
- `README.md` - Setup and usage instructions

**Services:**
- **MongoDB** - Document database (port 27017)

**Connection:**
- Host: `localhost`
- Port: `27017`
- Username: `root`
- Password: `rootpassword`

---

### Neo4j

Graph database for connected data.

**Files:**
- `docker-compose.yml` - Neo4j configuration
- `README.md` - Setup and usage instructions

**Services:**
- **Neo4j** - Graph database (ports 7474, 7687)

**Access:**
- **Neo4j Browser**: http://localhost:7474
- **Bolt Protocol**: bolt://localhost:7687
- **Credentials**: neo4j / password

---

### Postgres

Relational database for structured data.

**Files:**
- `docker-compose.yml` - PostgreSQL configuration
- `README.md` - Setup and usage instructions

**Services:**
- **PostgreSQL** - Relational database (port 5432)

**Configuration:**
| Variable | Default |
|----------|---------|
| POSTGRES_USER | postgres |
| POSTGRES_PASSWORD | postgres |
| POSTGRES_DB | postgres |
| Port | 5432 |

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

### RabbitMQ

Enterprise-grade message broker with management UI.

**Files:**
- `docker-compose.yml` - RabbitMQ configuration
- `README.md` - Setup and usage instructions

**Services:**
- **RabbitMQ** - Message broker (ports 5672, 15672)

**Access:**
- AMQP: `localhost:5672`
- Management UI: http://localhost:15672 (guest/guest)

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

### RustFS

S3-compatible object storage server for local development.

**Files:**
- `docker-compose.yml` - RustFS configuration
- `README.md` - Setup and usage instructions

**Services:**
- **RustFS** - S3-compatible storage (ports 9000, 9001)

**Access:**
- **API**: http://localhost:9000
- **Console**: http://localhost:9001

**Credentials:**
- **Access Key**: `rustfsadmin`
- **Secret Key**: `rustfsadmin`

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


