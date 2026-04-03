# Langfuse Self-Hosted

Self-hosted Langfuse instance using Docker Compose.

## Services

| Service | Port | Description |
|---------|------|-------------|
| langfuse-web | 3000 | Langfuse web UI |
| minio | 9090 | S3-compatible object storage (console) |
| clickhouse | 8123, 9000 | Analytics database |
| redis | 6379 | Caching and queue |
| postgres | 5432 | Primary database |

## Quick Start

1. Copy environment variables:
   ```bash
   cp .env.example .env
   ```

2. Update the `# CHANGEME` placeholders in `.env` with secure values:
   - `SALT` and `ENCRYPTION_KEY`
   - `NEXTAUTH_SECRET`
   - `CLICKHOUSE_PASSWORD`
   - `MINIO_ROOT_PASSWORD`
   - `REDIS_AUTH`
   - `POSTGRES_PASSWORD`

3. Generate an encryption key:
   ```bash
   openssl rand -hex 32
   ```

4. Start services:
   ```bash
   docker compose up -d
   ```

5. Access Langfuse at http://localhost:3000

## Security Notes

- Ports 3000 and 9090 are exposed externally
- All other services are bound to `127.0.0.1` for local access only
- Update all `# CHANGEME` credentials before production use
