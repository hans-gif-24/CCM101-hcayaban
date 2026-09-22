☁️ Laboratory Activity 4 — Mission 4: The Cloud-Native Engineer
📖 Mission Overview

After completing the previous multi-cloud activities, I continued my learning journey as a Cloud-Native Engineer at CloudNova Technologies.

This laboratory helped me understand containerization and how it differs from traditional Virtual Machines (VMs). Containers are commonly used in modern cloud applications because they are lightweight, portable, and allow applications to start quickly.

Through the KillerCoda Playground, I studied the basics of virtualization and containers, practiced important Docker commands, and deployed a web server using an Nginx container.

💡 Key Idea: Traditional system administrators mainly manage servers, while cloud-native engineers focus more on the applications and services running in the cloud environment.

🎯 Objectives

After completing this laboratory, I was able to:

Describe the differences between Virtual Machines and containers.

Access and use the Docker environment in KillerCoda.

Run basic Docker Command Line Interface (CLI) commands.

Download, start, check, stop, and remove an Nginx container.

Record Docker operations using properly formatted Markdown.

Add technical documentation to my GitHub Cloud Computing Portfolio.

💻 Docker Commands Executed

The following commands were used during Checkpoints 3, 4, and 5.

Checkpoint 3 — Verifying Docker Installation

Command

	

Description




docker --version

	

Shows the installed Docker version.




docker info

	

Displays details about the Docker environment, such as containers, images, storage, and system settings.

Result Observed:

Docker version 29.1.3 was available in the Ubuntu 24.04.4 LTS environment. Since the playground was newly started, it initially had no containers or images.

Screenshot Description — Checkpoint 3.1: The terminal showed the Docker version, confirming that Docker was installed and ready to use.

Screenshot Description — Checkpoint 3.2: The docker info command displayed details about the Docker system, including the operating system, number of containers and images, and other configuration information.

Checkpoint 4 — Running the First Container

In this checkpoint, I used Docker to deploy an Nginx web server inside a container.

Command

	

Description




docker pull nginx

	

Downloads the official Nginx image from Docker Hub.




docker run -d -p 8080:80 --name nginx-server nginx

	

Starts an Nginx container in the background and maps host port 8080 to container port 80.




curl http://localhost:8080

	

Sends a request to check if the Nginx web server is working.

Result Observed:

The terminal displayed the HTML content of the Nginx welcome page. This showed that the web server had been deployed successfully and was responding from inside the Docker container.

Checkpoint 5 — Managing the Container Lifecycle

This checkpoint allowed me to practice the basic steps for managing a Docker container.

#

	

Command

	

Description




1

	

docker ps

	

Lists running containers and allows me to check whether nginx-server is active.




2

	

docker stop nginx-server

	

Stops the running Nginx container.




3

	

docker ps -a

	

Shows all containers, including stopped ones, so I can verify that the container has exited.




4

	

docker rm nginx-server

	

Deletes the stopped Nginx container from the Docker environment.




5

	

docker ps -a

	

Checks the container list again to confirm that the removed container is no longer present.

🧠 Skills Learned

Through this laboratory activity, I developed practical knowledge and skills in the following areas:

Virtualization vs. Containers: Understood how VMs and containers differ in startup time, size, and resource usage.

KillerCoda Playground: Gained experience working with a cloud-based Docker environment.

Docker CLI: Practiced commands for downloading images, running containers, mapping ports, and checking Docker information.

Container Lifecycle: Learned how to create, view, stop, and remove containers.

Web Server Deployment: Successfully used a Docker container to run an Nginx web server.

Technical Documentation: Improved my ability to write organized technical reports using Markdown and GitHub.

Troubleshooting: Learned how to use KillerCoda's Traffic feature to access exposed ports when the web server is not directly reachable through local localhost:8080.

⚠️ Challenges Encountered

One of the challenges I faced during this activity was becoming familiar with Docker commands and their functions. At first, commands like docker run, docker ps, docker stop, and docker rm were new to me, making it harder to monitor and manage containers.

I addressed this by:

Following the laboratory instructions carefully.

Practicing the commands in the KillerCoda environment.

Checking the terminal output after each command.

By doing these steps, I became more familiar with how Docker commands work and how they are used to create, view, stop, and remove containers.

This experience helped me become more confident using the Docker command line and gave me a clearer understanding of container management.

📚 References

Amazon Web Services. (2025, December 8). Containers vs virtual machines: Understanding the difference. AWS Builder Center. https://builder.aws.com/content/2lngiMeN3ZNKY4AFS5ih5lGVGN0/containers-vs-virtual-machines-understanding-the-difference

CleanStart. (2026, June 9). Containers vs virtual machines: Architecture, security, and performance compared. https://www.cleanstart.com/knowledge-hub/containers-vs-virtual-machines

Docker. (n.d.). Docker documentation. https://docs.docker.com/

KillerCoda. (n.d.). KillerCoda playgrounds. https://killercoda.com/playgrounds
