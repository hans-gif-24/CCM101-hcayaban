# ☁️ Mission 10: The Enterprise Cloud Architect

## 📌 Project Overview

This repository contains the final project for **CCM101 – Cloud Computing**. It demonstrates the implementation of a multi-tier application hosted on an Ubuntu Server virtual machine, covering essential cloud computing tasks such as infrastructure planning, server configuration, application deployment, security implementation, automation, and technical documentation.

The project uses **Docker and Docker Compose** to deploy and manage interconnected application services. It also incorporates persistent database storage to protect important information and ensure that data is retained even after the virtual machine is restarted.

To strengthen server security, **UFW (Uncomplicated Firewall)** is configured to manage incoming connections and restrict unauthorized access. A Bash script is also created and scheduled through **Cron** to automate regular administrative activities, including database backups and system monitoring.

Overall, this project combines the knowledge and practical skills developed throughout the Cloud Computing laboratory activities into one functional cloud-based deployment.

## 🎯 Project Objectives

The main objectives of this project are to:

- 🏗️ Design and document the cloud infrastructure and network setup.
- 💻 Install and configure an Ubuntu Server virtual machine.
- 🐳 Set up Docker and Docker Compose for container management.
- 🔗 Run a multi-tier application using at least two connected containers.
- 💾 Configure persistent storage to maintain database information.
- 🔐 Apply server protection through UFW using a default-deny incoming traffic policy.
- 🌐 Allow only the necessary ports for application access and SSH connections.
- ⚙️ Create an executable Bash script for automating administrative operations.
- ⏰ Configure Cron to run scheduled tasks automatically.
- 📚 Develop documentation for deployment, security, maintenance, and system recovery.

## 🛠️ Technology Stack

The table below lists the tools, platforms, and configurations involved in the deployment. Replace the placeholders with the actual technologies used in your environment.

| Component | Technology / Configuration |
|---|---|
| 💻 Host Machine | [Windows / Linux / macOS] |
| ⚙️ Hypervisor | [VirtualBox / VMware / Other] |
| 🖥️ Virtual Machine OS | Ubuntu Server [Version] |
| 🐳 Container Platform | Docker |
| 🔗 Container Orchestration | Docker Compose |
| 🌐 Application | [WordPress / Nextcloud / Other] |
| 🗄️ Database | [MySQL / MariaDB / PostgreSQL / Other] |
| 💾 Persistent Storage | Docker Named Volume: [Volume Name] |
| 🔐 Firewall | UFW |
| ⚙️ Automation | Bash Script and Cron |
| 🔑 Access Method | Web Browser and SSH |

## 🏗️ System Architecture

Place the finalized infrastructure diagram in this section and name the image file `architecture-diagram.png`.

The diagram should present the overall structure of the deployment and show how each component connects and interacts with the others.

The following components should be included:

- 💻 Host Computer
- ⚙️ Type 2 Hypervisor
- 🖥️ Ubuntu Server Virtual Machine
- 🔐 UFW Firewall
- 🐳 Docker and Docker Compose
- 🌐 Application Container
- 🗄️ Database Container
- 💾 Persistent Database Volume
- 🌍 Client Web Browser / Host Access

Make sure the diagram clearly illustrates the relationship between the physical computer, virtual machine, containerized services, network connections, and persistent database storage.

**Enterprise Cloud Architecture**

## 📁 Repository Contents

The repository contains the following files and resources:

```text
Laboratory-10-Enterprise-Cloud-Architect/
├── README.md
├── architecture-diagram.png
├── docker-compose.yml
├── automation-script.sh
├── operational-manual.md
└── final-reflection.md
```

## 🚀 Deployment Summary

The application runs inside the Ubuntu Server virtual machine and is deployed using Docker Compose. This setup makes it possible to manage the application and database containers together while keeping their configurations organized.

To launch the services, open the terminal and navigate to the folder containing the `docker-compose.yml` file. Then execute the following commands:

```bash
# Run all services in the background
docker compose up -d

# Check the current container status
docker compose ps

# Display the logs of the services
docker compose logs
```

To stop the currently running application services, execute:

```bash
docker compose down
```

⚠️ **Important:** Check the service names and settings in your actual Compose configuration before running these commands. Do not use `docker compose down -v` unless you deliberately intend to remove the named volumes and permanently delete their stored database information.

## 🔐 Security Configuration

The server's network protection is managed through **UFW (Uncomplicated Firewall)**, which controls the incoming and outgoing network connections.

A default-deny policy is applied to incoming traffic. This means that external connections are rejected unless specific rules allow them. Only the ports required for SSH administration and application access should be permitted.

The following commands demonstrate the firewall configuration:

```bash
# Set the default rule to block incoming traffic
sudo ufw default deny incoming

# Allow outgoing network connections
sudo ufw default allow outgoing

# Allow SSH access
sudo ufw allow OpenSSH

# Permit the application's required port
sudo ufw allow [APPLICATION_PORT]/tcp

# Turn on the firewall
sudo ufw enable

# Review the active firewall rules
sudo ufw status verbose
```

Before executing the commands, replace `[APPLICATION_PORT]` with the actual port number assigned to your application.

🔎 **Security Reminder:** Avoid making database ports publicly accessible unless absolutely necessary and properly documented. Internal database services should remain accessible only to authorized containers and systems.

## ⚙️ Automation and Scheduling

The `automation-script.sh` file contains the Bash commands used to automate selected system administration activities.

The following information should be documented to explain how the automation works:

- 📝 **Automated Task:** Describe the operation performed by the script, such as database backup, system monitoring, or log cleanup.
- ⏰ **Schedule:** Specify the frequency and time when the script is executed.
- 📂 **Storage Location:** Identify the directory where backup files or generated outputs are saved.
- ✅ **Verification:** Explain the steps used to confirm that the automation runs as expected.

First, grant the script permission to execute:

```bash
chmod +x automation-script.sh
```

Next, access the current user's Cron configuration:

```bash
crontab -e
```

Insert the appropriate schedule together with the full path of the automation script:

```bash
[MINUTE] [HOUR] * * * /absolute/path/to/automation-script.sh
```

Replace the placeholders with the actual schedule and absolute file path based on your server configuration.

## 📚 Project Documentation

Further technical information and project details are available in the following files:

- 📖 **Operational Manual** – Provides detailed procedures for system installation, application deployment, firewall setup, automation configuration, database backup, data recovery, and regular server maintenance.
- 📝 **Final Reflection** – Discusses the experiences, difficulties, achievements, and technical lessons gained from completing Mission 1 through Mission 10.

## 🧪 Testing and Verification

Use the following checklist to evaluate the deployment and confirm that the required configurations are working properly.

- [ ] 🖥️ Ubuntu Server starts and runs without problems.
- [ ] 🌐 The host computer successfully connects to the virtual machine.
- [ ] 🐳 Docker and Docker Compose are installed and operational.
- [ ] 🔗 Both application and database containers launch successfully.
- [ ] 🗄️ The application establishes a successful connection with the database.
- [ ] 💾 Stored database information remains available after restarting the virtual machine.
- [ ] 🔐 UFW is active and configured with a default-deny incoming policy.
- [ ] 🚪 Only the necessary incoming network ports are accessible.
- [ ] ⚙️ The Bash automation script runs successfully when executed manually.
- [ ] ⏰ Cron is configured correctly and the scheduled task has been tested.
- [ ] 📊 The infrastructure diagram and operational manual are included in the repository.

## 🛠️ Troubleshooting Notes

This section is intended for documenting technical difficulties encountered during the project, identifying their possible causes, and describing the solutions used to resolve them.

| ⚠️ Problem Encountered | 🔍 Possible Cause | 🔧 Solution Implemented |
|---|---|---|
| [Describe the issue] | [State the possible reason] | [Explain how it was resolved] |
| [Describe the issue] | [State the possible reason] | [Explain how it was resolved] |
