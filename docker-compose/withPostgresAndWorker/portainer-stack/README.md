# Portainer Ready Stack

This folder contains a Portainer-ready stack for n8n with Postgres.

## Files

- `docker-compose.yml` — stack definition with a custom Postgres build.
- `Dockerfile.postgres-init` — builds a Postgres image with the init script baked in.
- `init-data.sh` — PostgreSQL initialization script.
- `.env.example` — example environment variables.

## Deploy steps

1. Copy `.env.example` to `.env` and update values as needed.
2. Open Portainer and deploy a new stack from this folder.
3. Ensure the stack is allowed to build local images.

## Notes

- The Postgres healthcheck is intentionally relaxed to allow slow startup and recovery.
- The init script is baked into the custom Postgres image to avoid host bind-mount issues.
