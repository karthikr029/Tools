# Elastic Stack

Docker Compose setup for Elasticsearch, Kibana, and Logstash.

## Services

| Service | Port | Description |
|---------|------|-------------|
| Elasticsearch | 9200, 9300 | Search and analytics engine |
| Kibana | 5601 | Visualization dashboard |
| Logstash | 5044, 9600 | Log processing pipeline |

## Quick Start

```bash
docker compose up -d
```

## Access

- **Elasticsearch**: http://localhost:9200
  - Username: `elastic`
  - Password: `elastic123`

- **Kibana**: http://localhost:5601
  - Username: `kibana_system`
  - Password: `kibana123`

## Logstash Configuration

Place your Logstash configuration files in:
- Pipeline: `logstash/pipeline/*.conf`
- Settings: `logstash/config/logstash.yml`

## Useful Commands

```bash
# Start services
docker compose up -d

# View logs
docker compose logs -f

# Stop services
docker compose down

# Stop and remove volumes
docker compose down -v
```
