# ☁️ Laboratory Activity 6 — The Cloud Deployment Engineer

## 🎯 Mission Overview

This laboratory activity focuses on deploying a private cloud storage application using **Docker Compose**. The project uses Nextcloud as the main web application and MariaDB as its database.

Instead of creating and managing each container separately, I used a single YAML configuration file to define both services. This activity helped me understand how multiple containers work together and how Docker Compose makes application deployment easier and more organized.

## 🎯 Objectives

The main objectives of this laboratory activity are to:

* Understand the basic concept of a **two-tier application architecture**.
* Create a Docker Compose configuration using YAML.
* Deploy and manage multiple containers with Docker Compose.
* Access the Nextcloud setup page through a web browser.
* Learn about **Infrastructure as Code (IaC)** and its role in deployment.
* Improve my GitHub portfolio by adding technical documentation and screenshots.

## 💻 Commands Used

The following commands are used to prepare, deploy, and manage the application:

| **Command**                  | **Purpose**                                                      |
| ---------------------------- | ---------------------------------------------------------------- |
| `mkdir nextcloud-deployment` | Creates a new directory for the deployment project.              |
| `cd nextcloud-deployment`    | Moves into the project directory.                                |
| `nano docker-compose.yml`    | Creates or edits the Docker Compose configuration file.          |
| `docker-compose up -d`       | Starts the defined services in the background.                   |
| `docker-compose ps`          | Displays the status of the containers managed by Docker Compose. |
| `docker-compose down`        | Stops and removes the Compose containers and network.            |

## 🛠️ Skills and Knowledge Gained

Through this activity, I learned how to write YAML configuration files and follow the correct indentation required for Docker Compose. I also gained a better understanding of how an application container communicates with a separate database container.

Another important skill I practiced was deploying and managing multiple containers using Docker Compose. I learned how to check container status, configure port mapping, and access a web application through a browser.

This laboratory also introduced me to **Infrastructure as Code (IaC)**, which allows infrastructure and services to be defined through configuration files instead of being configured entirely by hand. Using this approach makes deployments easier to repeat, maintain, and document.

Finally, I improved my skills in writing technical documentation and organizing screenshots and project files in GitHub.

## 📂 Project Files

The `Laboratory-06-Cloud-Deployment-Engineer/` folder contains the following files and resources:

* `README.md` — Provides an overview of the laboratory, objectives, commands, and expected results.
* `multi-tier-architecture.md` — Explains the two-tier application architecture and how the application and database work together.
* `docker-compose-guide.md` — Documents the YAML configuration, deployment process, and Docker Compose commands.
* `reflection.md` — Contains my personal reflection and the lessons I learned.
* `screenshots/` — Stores screenshots showing the configuration, container status, and Nextcloud setup page.

## ✅ Expected Result

The expected result is a working Nextcloud application connected to a MariaDB database, with both services running in separate containers.

When the deployment is successful, I should be able to check the container status using Docker Compose and access the Nextcloud setup page through a web browser using port `8080`.

The application and database should communicate correctly, allowing Nextcloud to use MariaDB for its database operations.

**Verification note:** The deployment must be tested in the KillerCoda environment, and screenshots should be captured to provide evidence that the application is running correctly.

## 📝 Overall Reflection

Overall, this laboratory helped me understand how Docker Compose simplifies the deployment of applications that require multiple services. By defining Nextcloud and MariaDB in one configuration file, I learned how to organize and manage the application more efficiently.

I also gained practical knowledge of container communication, YAML configuration, port mapping, and Infrastructure as Code. These skills are useful for deploying cloud applications and managing services in a consistent way.

This activity further improved my confidence in using Docker tools and documenting technical work through GitHub. It also helped me understand how application deployment involves connecting different services rather than running a single container alone.

