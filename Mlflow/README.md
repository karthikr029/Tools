# MLflow with Docker Compose

This directory provides a **Docker Compose** setup for running **MLflow** locally with a **PostgreSQL** backend store and **RustFS** for S3-compatible artifact storage.

---

## Overview

- **MLflow Tracking Server**  
  Serves the REST API and UI (default: `http://localhost:8080`).

- **PostgreSQL**  
  Stores MLflow's metadata (experiments, runs, params, metrics).

- **RustFS Artifact Storage**  
  Stores model files and run artifacts.

## 1. Launch the Stack

Inside directory **mlflow/docker-compose**:

```bash
docker compose up -d
```

This will:

- Start PostgreSQL
- Start RustFS
- Start MLflow
- Create the S3 bucket if it doesn't exist

Check status:

```bash
docker compose ps
```

Tail logs:

```bash
docker compose logs -f
```

---

## 2. Access MLflow

Once running:

- Open `http://localhost:8080` (or the port defined in `.env`)
