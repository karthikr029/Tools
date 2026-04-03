# Solace PubSub+

Run with: `docker compose up -d`

## Access

- **UI**: http://localhost:8081
- **Messaging**: 55556 (AMQP), 1944 (SMF)

## Credentials

- Username: `admin`
- Password: `admin`
- VPN: `default`

## Ports

| Port | Protocol |
|------|----------|
| 8081 | HTTP (SEMP UI) |
| 55556 | AMQP |
| 1944 | SMF |

## Commands

```bash
docker compose up -d     # Start
docker compose down      # Stop
docker compose logs -f   # View logs
```