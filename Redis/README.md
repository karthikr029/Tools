# Redis Stack with RedisInsight

Docker Compose setup for local Redis development with GUI.

## Services

- **Redis** - In-memory database (port 6379)
- **RedisInsight** - Redis GUI (port 5540)

## Quick Start

```bash
docker compose up -d
```

## Access

- RedisInsight: http://localhost:5540
- Redis: localhost:6379

## Commands

```bash
docker compose up -d      # Start
docker compose down      # Stop
docker compose logs -f   # View logs
```

## Connect to Redis

RedisInsight auto-configures a connection to Redis named "Local Redis".
