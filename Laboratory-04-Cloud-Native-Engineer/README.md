# ☁️ Laboratory Activity 4 — Mission 4: The Cloud-Native Engineer

## 📖 Mission Overview

In this laboratory, I continued my learning journey as a Cloud-Native Engineer at CloudNova Technologies. I explored containerization and learned how it differs from traditional Virtual Machines (VMs).

Containers are lightweight, portable, and can start applications quickly. Using the KillerCoda Playground, I studied the basics of virtualization and containers, practiced Docker commands, and deployed an Nginx web server inside a container.

💡 **Key Idea:** Traditional system administrators mainly manage servers, while cloud-native engineers focus more on the applications and services running in the cloud.

---

## 🎯 Objectives

After completing this laboratory, I was able to:

- Explain the differences between Virtual Machines and containers.
- Access and use the Docker environment in KillerCoda.
- Execute basic Docker Command Line Interface (CLI) commands.
- Download, run, monitor, stop, and remove an Nginx container.
- Document Docker operations using Markdown.
- Improve my GitHub Cloud Computing Portfolio through technical documentation.

---

## 💻 Docker Commands Executed

The following commands were used during Checkpoints 3, 4, and 5.

### Checkpoint 3 — Checking the Docker Installation

| **Command** | **Description** |
|---|---|
| `docker --version` | Displays the installed Docker version. |
| `docker info` | Shows information about the Docker environment, including containers, images, storage, and system settings. |

**Result Observed:**

The Docker environment showed version **29.1.3** running on Ubuntu 24.04.4 LTS. Since the environment was newly created, it initially had 0 containers and 0 images.

**Screenshot Evidence:**

- `docker-version.png` — Shows the Docker version and confirms that Docker is available.
- The terminal output of `docker info` shows details about the Docker environment, including the operating system, container count, and image count.

### Checkpoint 4 — Deploying the First Container

In this checkpoint, I deployed an Nginx web server using Docker.

| **Command** | **Description** |
|---|---|
| `docker pull nginx` | Downloads the official Nginx image from Docker Hub. |
| `docker run -d -p 8080:80 --name nginx-server nginx` | Creates and starts an Nginx container in the background while mapping host port 8080 to container port 80. |
| `curl http://localhost:8080` | Sends an HTTP request to check if the Nginx web server is responding. |

**Result Observed:**

The terminal displayed the HTML content of the Nginx welcome page. This confirmed that the web server was running inside the Docker container and responding to requests.

**Screenshot Evidence:**

- `nginx-running.png` — Shows the successful response from the Nginx web server.

### Checkpoint 5 — Managing the Container Lifecycle

This checkpoint focused on managing the Nginx container.

| **#** | **Command** | **Description** |
|---:|---|---|
| 1 | `docker ps` | Lists running containers and checks if `nginx-server` is active. |
| 2 | `docker stop nginx-server` | Stops the running Nginx container. |
| 3 | `docker ps -a` | Lists all containers, including stopped ones, to check the container's status. |
| 4 | `docker rm nginx-server` | Removes the stopped Nginx container. |
| 5 | `docker ps -a` | Checks the container list again to verify that `nginx-server` has been removed. |

**Screenshot Evidence:**

- `container-lifecycle.png` — Shows the commands used to stop, check, and remove the Nginx container.

---

## 🧠 Skills Learned

Through this laboratory activity, I gained practical experience in the following areas:

- **Virtualization vs. Containers:** Learned how VMs and containers differ in startup time, size, and resource usage.
- **KillerCoda Playground:** Practiced using a cloud-based Docker environment.
- **Docker CLI:** Used commands to download images, run containers, map ports, and check Docker information.
- **Container Lifecycle:** Learned how to list, stop, and remove containers.
- **Web Server Deployment:** Practiced running an Nginx web server inside a container.
- **Technical Documentation:** Improved my ability to organize technical information using Markdown and GitHub.
- **Troubleshooting:** Learned to use KillerCoda's Traffic feature to access exposed ports when the web server cannot be reached directly through `localhost:8080`.

---

## ⚠️ Challenges Encountered

One of the challenges I faced was understanding the different Docker commands and their functions. At first, commands such as `docker run`, `docker ps`, `docker stop`, and `docker rm` were unfamiliar to me, which made managing containers a little difficult.

I addressed this by:

1. Following the laboratory instructions carefully.
2. Practicing each command in the KillerCoda environment.
3. Observing the terminal output after running each command.

Through these steps, I became more familiar with how Docker commands are used to create, view, stop, and remove containers.

This experience helped me become more confident using the Docker command line and improved my understanding of container management.

---

## 📚 References

- Amazon Web Services. (2025, December 8). *Containers vs virtual machines: Understanding the difference.* AWS Builder Center. https://builder.aws.com/content/2lngiMeN3ZNKY4AFS5ih5lGVGN0/containers-vs-virtual-machines-understanding-the-difference
- CleanStart. (2026, June 9). *Containers vs virtual machines: Architecture, security, and performance compared.* https://www.cleanstart.com/knowledge-hub/containers-vs-virtual-machines
- Docker. (n.d.). *Docker documentation.* https://docs.docker.com/
- KillerCoda. (n.d.). *KillerCoda playgrounds.* https://killercoda.com/playgrounds
