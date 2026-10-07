
# Docker Compose Guide

## The Services Block

The `services:` block defines the containers that will be created and managed by Docker Compose. In this project, there are two services: `database` for MariaDB and `app` for Nextcloud.

## Database Service

The database service uses the `mariadb:10.6` Docker image. Environment variables are used to configure the MariaDB root password, database password, database name, and database user.

## Application Service

The application service uses the `nextcloud` Docker image. It also maps port `8080` on the host to port `80` inside the container so that the Nextcloud web interface can be accessed through a browser.

## How Nextcloud Finds the Database

The Nextcloud container uses the following environment variable:

```yaml
- MYSQL_HOST=database
