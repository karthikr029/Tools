# Kafka Local Setup

Run a local Kafka cluster with AKHQ 

## Pre-requisites
1. Requires Docker to be installed on the machine and running

## Instructions

1. Clone the repository
2. create a local directory for kafka to persist data using `mkdir -p data`
3. Run `docker compose up -d`
4. Access the AKHQ UI at `http://localhost:8080/ui/docker-kafka-server/topic`