# PostgreSQL

Docker Compose setup for PostgreSQL.

## Quick Start

```bash
cd Postgres
docker compose up -d
```

## Configuration

| Variable | Default |
|----------|---------|
| POSTGRES_USER | postgres |
| POSTGRES_PASSWORD | postgres |
| POSTGRES_DB | postgres |
| Port | 5432 |

## Connect

```bash
psql -h localhost -U postgres -d postgres
```
