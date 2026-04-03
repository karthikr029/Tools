# RustFS

S3-compatible object storage server for local development.

## Quick Start

```bash
docker compose up -d
```

## Access

- **API**: http://localhost:9000
- **Console**: http://localhost:9001

## Credentials

- **Access Key**: `rustfsadmin`
- **Secret Key**: `rustfsadmin`

## Connection

Use any S3-compatible client:

```bash
# Using AWS CLI
aws configure set aws_access_key_id rustfsadmin
aws configure set aws_secret_access_key rustfsadmin
aws configure set region us-east-1

# List buckets
aws s3 ls --endpoint-url http://localhost:9000
```

## Stop

```bash
docker compose down
```

To also remove data:

```bash
docker compose down -v
```
