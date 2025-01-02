# PostgreSQL with Adminer - Local Development Environment

This setup provides a PostgreSQL database server with Adminer for local development.

## Services

### PostgreSQL
- **Version**: Latest
- **Port**: 5432
- **Credentials**:
  - Username: postgres
  - Password: postgres
  - Database: dev_db
- **Data Persistence**: Data is stored in `./postgres_data` directory

### Adminer
- **Version**: Latest
- **Port**: 8080
- **Theme**: Dracula
- **URL**: http://localhost:8080

## Getting Started

1. Start the services:
```bash
docker-compose up -d
```

2. Access Adminer:
   - Open http://localhost:8080 in your browser
   - Use these connection details:
     - System: PostgreSQL
     - Server: postgres
     - Username: postgres
     - Password: postgres
     - Database: dev_db

## Health Checks

PostgreSQL server includes health checks that:
- Run every 10 seconds
- Timeout after 5 seconds
- Retry up to 5 times

## Network

Services run on a dedicated bridge network named `postgres_dev_network`.

## Data Persistence

Database data is persisted in the `./postgres_data` directory relative to the compose file.
