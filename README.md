# tomcat-postgres-docker

Project repository with docker configuration for spring webapp with tomcat and postgres

## Requirements

- Docker

## Boostrap

Project bootstrap is pretty simple.
With docker installed on your machine, run the following command:

```bash
docker-compose up
```

A new container will boot with following services:
- Postgres 9.1
- Tomcat 8.0
- Apache

## Services
### Postgres

Postgres will be exposed on port `5432` and will be accessible for container services at host `db`.
At first startup, sql files listed in docker-compose under `volumes` will be used for database creations and seeding.

### Apache

Apache is exposed on port `90` and it just acts as proxy for http calls redirection to tomcat.

### Tomcat

Tomcat is exposed on port `9090` and can be debugged using port `9000`.
You just needs to setup a remote debugging configuration which listens at port `9000`.