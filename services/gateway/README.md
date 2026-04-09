# API Gateway

Reverse proxy and entry point for all client requests.

## Responsibility

- TLS termination
- JWT authentication enforcement
- CORS policy
- Rate limiting (100 req/min per user)
- Request routing to internal services

## Technology

Nginx or Traefik (see [architecture.md](../../specs/architecture.md) §5).

## Port

`:443` (production)
