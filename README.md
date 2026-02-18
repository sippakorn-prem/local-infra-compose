# Docker Compose – Local dev stack

A single `docker-compose` setup to run common databases and services on your machine for development.

## Services

| Service        | Image              | Port | Use for              |
|----------------|--------------------|------|----------------------|
| **Redis**      | redis:7.4          | 6379 | Cache, sessions      |
| **PostgreSQL** | postgres:17        | 5432 | Relational database  |
| **MariaDB**    | mariadb:12.2       | 3306 | MySQL-compatible DB  |
| **MSSQL**      | Azure SQL Edge     | 1433 | SQL Server           |
| **Elasticsearch** | elasticsearch:8.17.0 | 9200 | Search, logs         |

## Quick start

1. Copy env example and set passwords (and DB name if you want):

   ```bash
   cp .env.example .env
   # Edit .env with your values
   ```

2. Start everything (run from this directory so `.env` is loaded):

   ```bash
   docker compose up -d
   ```

3. Stop:

   ```bash
   docker compose down
   ```

Data is stored in Docker volumes so it survives restarts.
