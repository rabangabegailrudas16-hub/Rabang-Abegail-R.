
# Multi-Tier Architecture

## What is a Two-Tier Architecture?

A two-tier architecture separates an application into two main layers: the web/application tier and the database tier. In this laboratory, Nextcloud acts as the web/application tier while MariaDB acts as the database tier.

## The Web/Application Tier

The web/application tier is responsible for serving the application's user interface and handling HTTP requests from users. In this deployment, Nextcloud provides the private cloud storage interface and communicates with the database when information is needed.

## The Database Tier

The database tier is responsible for storing persistent information used by the application. MariaDB stores information such as user accounts, configuration data, and file metadata required by Nextcloud.

## Why Separate Them?

Separating the web application and database into different containers makes the system easier to manage and maintain. Each container has a specific responsibility, and one component can be updated or managed without placing everything inside a single container.
