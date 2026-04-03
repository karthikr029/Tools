# HashiCorp Vault Docker Setup

Run the latest version of HashiCorp Vault locally using Docker Compose.

## Quick Start

```bash
docker compose up -d
```

## Access Vault

- **UI**: http://localhost:8200
- **Token**: `root`

## Commands

```bash
# Start
docker compose up -d

# Stop
docker compose down

# Stop and remove volumes
docker compose down -v

# View logs
docker compose logs -f vault
```

## Note

This configuration uses Vault in dev mode. Do not use dev mode in production.
