# Docker Compose Guide

## Introduction

Docker Compose is a tool used to define and manage multiple Docker containers using a single YAML configuration file. In this laboratory activity, Docker Compose was used to deploy a two-tier private cloud storage application consisting of Nextcloud and MariaDB.

The configuration was written inside a file named `docker-compose.yml`.

## The `services:` Block

The `services:` block defines the different containers or services that will be created and managed by Docker Compose.

In this project, there are two services:

* `database` – runs the MariaDB database.
* `app` – runs the Nextcloud application.

Each service has its own Docker image and configuration.

## Database Service

The database service is defined as:

```yaml
database:
  image: mariadb:10.6
```

The `image` specifies the Docker image that will be used for the database container. In this case, MariaDB version 10.6 is used.

The database also uses environment variables:

```yaml
environment:
  - MYSQL_ROOT_PASSWORD=cloudnova_root
  - MYSQL_PASSWORD=cloudnova_pass
  - MYSQL_DATABASE=nextcloud_db
  - MYSQL_USER=nextcloud_user
```

These variables configure the MariaDB database with a root password, database password, database name, and database user.

## Nextcloud Application Service

The application service is defined as:

```yaml
app:
  image: nextcloud
```

This tells Docker Compose to use the official Nextcloud image for the application container.

The application also exposes port 80 from the container through port 8080 on the host:

```yaml
ports:
  - 8080:80
```

This allows the Nextcloud web interface to be accessed through port `8080`.

## Environment Variables

The Nextcloud container uses the following environment variables:

```yaml
environment:
  - MYSQL_PASSWORD=cloudnova_pass
  - MYSQL_DATABASE=nextcloud_db
  - MYSQL_USER=nextcloud_user
  - MYSQL_HOST=database
```

These variables provide Nextcloud with the information it needs to connect to the MariaDB database.

## How Nextcloud Finds the Database

The important setting is:

```yaml
- MYSQL_HOST=database
```

The value `database` is the service name of the MariaDB container.

Docker Compose creates a network for the services in the Compose file. Because of this, containers can communicate with each other using their service names.

Therefore, Nextcloud can find the MariaDB container by using:

```text
database
```

as the database host.

The application does not need to use an IP address because Docker Compose handles the service-to-service communication through its internal network.

## Port Mapping

The following configuration is used:

```yaml
ports:
  - 8080:80
```

The first number, `8080`, is the port on the host machine.

The second number, `80`, is the port inside the Nextcloud container.

This means
