# 🔐 Firewall Configuration

## Mission 8: The Cloud Security Engineer

### 1. 🔑 Allow SSH

```bash
sudo ufw allow ssh
```

This command allows SSH connections so administrators can access and manage the server remotely.

### 2. 🛡️ Set the Default Firewall Policies

```bash
sudo ufw default deny incoming
sudo ufw default allow outgoing
```

The first command blocks incoming connections unless they are allowed by a firewall rule. The second command permits outgoing connections from the server by default.

### 3. ⚙️ Activate and Check UFW

```bash
sudo ufw enable
sudo ufw status verbose
```

These commands turn on the firewall and show its status, default policies, and current rules.

### 4. 🌐 Allow the Web Application

```bash
sudo ufw allow 8080/tcp
```

This command allows incoming TCP connections through port 8080, which is used by the Nginx web application.

### 5. 📋 Check the Firewall Rules

```bash
sudo ufw status numbered
```

This command displays all configured firewall rules with numbers, making them easier to check and manage.

### 6. 🧪 Test the Web Application

```bash
curl http://localhost:8080
```

If the application is running correctly, this command displays the HTML content provided by the Nginx web server.

### ⚠️ Security Warning

If the firewall is enabled before allowing SSH connections, remote access may be blocked by the default incoming policy. This can make it difficult for an administrator to manage the server remotely.

### 📊 Final Configuration

| **Setting** | **Configuration** |
|---|---|
| Firewall | UFW |
| Incoming traffic | Denied by default |
| Outgoing traffic | Allowed by default |
| SSH | Allowed |
| Web application | TCP port 8080 allowed |

### 💡 Recommendation

Check firewall rules regularly and remove access permissions for services that are no longer required. Only allow the connections needed for the server to operate properly and securely.
