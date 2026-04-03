# Neo4j Local Development

Run Neo4j locally using Docker.

## Quick Start

```bash
docker compose up -d
```

## Access

- **Neo4j Browser**: http://localhost:7474
- **Bolt Protocol**: bolt://localhost:7687

## Credentials

- **Username**: `neo4j`
- **Password**: `password`

## Stop

```bash
docker compose down
```

To also remove data:

```bash
docker compose down -v
```
