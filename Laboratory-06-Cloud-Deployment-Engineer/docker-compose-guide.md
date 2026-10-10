# 🐳 Docker Compose Guide

## 📖 Introduction

Docker Compose is a tool that helps developers and cloud engineers configure and run multiple containers using a single YAML file. In this laboratory activity, I used Docker Compose to set up **Nextcloud and MariaDB** as connected services. This approach makes deployment more organized because both services can be managed through one configuration file instead of starting each container individually.

## 1. Understanding the `services:` Block

The `services:` section defines the containers needed for an application. In this project, the configuration includes two services: `database` and `app`.

The `database` service uses the `mariadb:10.6` image and contains the settings needed to configure the database name and login credentials. Meanwhile, the `app` service uses the Nextcloud image and maps port `8080` on the host to port `80` inside the container.

These two services work together to provide a functioning Nextcloud application that uses MariaDB to store its database information.

## 2. How Nextcloud Connects to the Database

The environment variable `MYSQL_HOST=database` tells Nextcloud which service to contact when connecting to the database.

Docker Compose allows containers to communicate with one another through service names on their shared network. Since the MariaDB service is named `database`, Nextcloud can use that name to locate the database without needing to know its IP address manually.

The database name, username, and password must also be configured consistently between the two services. If these settings do not match, Nextcloud may fail to establish a database connection.

## 3. Difference Between `docker run` and `docker-compose up -d`

The `docker run` command is mainly used to create and start an individual container. It allows users to specify settings such as the image, ports, and environment variables directly in the terminal. However, managing multiple related containers may require several separate commands.

On the other hand, `docker-compose up -d` reads the `docker-compose.yml` file and starts the services defined in the configuration. The `-d` option runs the containers in the background, allowing the terminal to remain available for other commands.

Using Docker Compose makes it easier to deploy and manage applications that require multiple connected services. It also allows the same configuration to be reused for future deployments.

## 4. Understanding Infrastructure as Code (IaC)

**Infrastructure as Code (IaC)** is an approach that uses configuration files to define and manage infrastructure instead of relying only on manual setup.

In this activity, the `docker-compose.yml` file describes the required services, Docker images, port mappings, and environment variables for Nextcloud and MariaDB.

Keeping these settings in a configuration file makes the deployment easier to review, modify, share, and reproduce. The file can also be stored in GitHub so that changes can be tracked and the configuration can be maintained alongside the project's documentation.

However, sensitive information, such as database passwords, should be protected and should not be published in a public repository.

## 📝 Conclusion

This activity helped me understand how Docker Compose can simplify the deployment of applications that depend on multiple services. By using one YAML configuration file, I learned how to define Nextcloud and MariaDB, understand their communication, and manage their deployment more efficiently.

I also gained a better understanding of Infrastructure as Code and how configuration files improve consistency and maintainability. These concepts are useful for deploying cloud applications because they make infrastructure easier to organize, manage, and reproduce.

