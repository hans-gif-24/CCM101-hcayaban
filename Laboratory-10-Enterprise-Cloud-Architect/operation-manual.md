# 📖 OPERATIONAL MANUAL: CLOUD ARCHITECTURE

This manual serves as a technical reference for managing and maintaining the deployed cloud infrastructure. It contains the necessary access procedures, service descriptions, configurations, and basic administrative instructions for each container included in the architecture.

## 🔑 Root User Account

The following credentials are intended for the primary administrative account:

- **Username:** `[ROOT_USERNAME]`
- **Password:** `[ROOT_PASSWORD]`

Keep administrative credentials secure and accessible only to authorized personnel.

## 🔐 SSH Access

To connect to the Ubuntu Server remotely through SSH, use the following command:

```bash
ssh vboxuser@[VM.LOCAL.IP]
```

Replace `[VM.LOCAL.IP]` with the actual local IP address assigned to your virtual machine based on its current network configuration.

- **Username:** `vboxuser`
- **Password:** `[SSH_PASSWORD]`

It is recommended to establish an SSH connection as soon as the Ubuntu Server becomes available. This provides remote administrative access while allowing the virtual machine to operate primarily as the host for the deployed services.

### Custom Host Configuration

If the virtual machine is transferred to another computer or connected to a different network, its IP address may change. In such cases, the local hosts file may need to be updated to ensure that the custom domain names continue pointing to the correct server.

For Windows users, the hosts file is located at:

```text
C:\Windows\System32\drivers\etc\hosts
```

Open the file using administrator privileges and add the following entries:

```text
[VM.LOCAL.IP] vault.cloudnova.server
[VM.LOCAL.IP] gitea.cloudnova.server
[VM.LOCAL.IP] pihole.cloudnova.server
```

Replace `[VM.LOCAL.IP]` with the current local IP address of the Ubuntu Server.

Whenever possible, use the configured DNS server instead of manually modifying the hosts file. Refer to the Pi-hole section for additional information about DNS configuration and network-related adjustments.

---

## 🏗️ Container Architecture

The cloud environment consists of five interconnected services, each responsible for a specific function within the infrastructure.

The deployed containers include:

- 🐙 **Gitea** – Self-hosted Git repository and development platform.
- 🔐 **Vaultwarden** – Password and sensitive information management.
- 🛡️ **Pi-hole** – DNS filtering and custom domain resolution.
- 🌐 **Nginx** – Reverse proxy and HTTPS connection management.
- 🗄️ **PostgreSQL** – Database service for Gitea and Vaultwarden.

## 🐙 1. Gitea

Gitea provides a self-hosted alternative to GitHub, allowing developers and employees to manage source code, repositories, and development projects within the organization's own infrastructure.

Compared to the other services, Gitea generally requires less frequent operational maintenance. Most administrative activities involve managing user accounts, removing inactive users, deleting unnecessary repositories, and maintaining the platform.

Employees primarily use the service for their development-related activities, while administrative tasks are handled through the root account.

### Account Information

**Administrative Account**
- Username: `[GITEA_ADMIN_USERNAME]`
- Password: `[GITEA_ADMIN_PASSWORD]`

**Test Account**
- Username: `John_Doe`
- Password: `[TEST_ACCOUNT_PASSWORD]`

Keep administrative access restricted and review user accounts and repositories regularly.

## 🔐 2. Vaultwarden

Vaultwarden is used to manage and securely store passwords and other sensitive information for employees and authorized personnel.

New user registration can be controlled through the `SIGNUPS_ALLOWED` environment variable.

To enable account registration temporarily, change the configuration to:

```yaml
SIGNUPS_ALLOWED: "true"
```

For the current deployment, this setting is disabled:

```yaml
SIGNUPS_ALLOWED: "false"
```

This configuration restricts new registrations and allows the designated root account to manage the stored credentials.

### Root Account Information

- Email: `root@cloudnova.server`
- Password: `[VAULTWARDEN_PASSWORD]`

Only authorized personnel should have access to the administrative account and stored information.

## 🛡️ 3. Pi-hole

Pi-hole functions as a DNS filtering service within the cloud infrastructure. It provides two primary capabilities: blocking unwanted advertising domains and resolving custom domain names used to access the hosted services.

Through its DNS functionality, users within the configured network can access services using their assigned domain names instead of entering the virtual machine's IP address directly.

This setup is intended to keep the services accessible within the local network rather than exposing them directly to the public internet.

### Administrative Access

- Password: `[PIHOLE_ADMIN_PASSWORD]`

### Network and DNS Configuration

When the server is moved to another network, the custom DNS records may need to be updated to match the new IP address of the Ubuntu Server.

If access to the Pi-hole administration interface is necessary during this process, the following port mapping may be added temporarily to the Docker configuration:

```yaml
ports:
  - "8081:80"
```

This allows the Pi-hole web interface to be accessed through port `8081` while making the necessary DNS adjustments.

After completing the configuration, remove the temporary port mapping if it is no longer needed.

## 🌐 4. Nginx

Nginx serves as the reverse proxy for the deployed services. It manages incoming requests and directs them to the appropriate containers based on their configured domain names.

It also works together with Pi-hole to support access through custom local domain names.

Most Nginx-related maintenance involves two main areas:

- **Nginx Configuration:** The `nginx.conf` file contains the reverse proxy rules and service routing configurations.
- **SSL Certificate Management:** OpenSSL is used to manage and renew the certificates required for HTTPS connections.

### Certificate Maintenance

If an SSL certificate expires, possibly because the scheduled renewal process stopped working, the certificate must be renewed using the appropriate OpenSSL procedure.

If certificate files are relocated, review the Nginx configuration and update the certificate paths accordingly.

Make sure that the configured certificate locations match the actual files available on the server.

Regularly check certificate validity and confirm that HTTPS connections are functioning properly.

## 🗄️ 5. PostgreSQL

PostgreSQL serves as the database management system for both Gitea and Vaultwarden. It stores the information required by these applications to operate correctly.

An initialization script named `init-db.sh` is included in the Docker Compose configuration to prepare the database required by Gitea during the initial setup.

### Creating a New Database

Additional databases can be created directly through the PostgreSQL command-line interface.

Use the following SQL command:

```sql
CREATE DATABASE [DATABASE_NAME];
```

Replace `[DATABASE_NAME]` with the desired database name.

### Accessing PostgreSQL

To open an interactive PostgreSQL session inside the database container, use:

```bash
docker exec -it [POSTGRES_CONTAINER] psql -U [DATABASE_USER] -d postgres
```

Replace the placeholders with the actual container name and database username configured in your environment.

Once connected, PostgreSQL commands and SQL statements can be executed directly.

For example:

```sql
-- Display available databases
\l

-- Connect to a specific database
\c [DATABASE_NAME]

-- Display tables
\dt

-- Exit the PostgreSQL terminal
\q
```

Always verify database names and user permissions before making changes to existing records or configurations.

---

## 🛠️ General Maintenance Reminders

To keep the cloud architecture operating properly, consider the following maintenance practices:

- Regularly review administrative accounts and access permissions.
- Keep passwords and other sensitive information protected.
- Check the status of all Docker containers.
- Verify that Gitea and Vaultwarden can communicate with PostgreSQL.
- Confirm that Pi-hole DNS records point to the correct server IP.
- Review Nginx configurations and check SSL certificate expiration dates.
- Test domain resolution and HTTPS accessibility.
- Maintain regular database backups.
- Review system logs whenever unexpected errors occur.

**Important:** Always create a backup of important configuration files and database information before performing major changes to the infrastructure.

## 📝 Final Note

This operational manual is intended to guide administrators in accessing, configuring, and maintaining the CloudNova infrastructure. Following the procedures and maintenance recommendations provided in this document can help ensure that the deployed services remain organized, accessible, and properly managed.
