
# Laboratory 06 – Cloud Deployment Engineer

## Mission Overview

In this laboratory activity, I deployed a multi-tier private cloud storage application using Docker Compose. The application consists of Nextcloud as the web/application tier and MariaDB as the database tier.

## Objectives

- Understand multi-tier application architecture.
- Create a Docker Compose YAML configuration.
- Deploy multiple containers using Docker Compose.
- Connect Nextcloud with a MariaDB database.
- Practice Infrastructure as Code (IaC).
- Document the deployment process using Markdown.

## Commands Executed

```bash
mkdir nextcloud-deployment
cd nextcloud-deployment
nano docker-compose.yml
docker-compose up -d
docker-compose ps
docker-compose down
