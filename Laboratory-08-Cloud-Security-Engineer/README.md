# 🔐 Mission 8: The Cloud Security Engineer

## 📌 Mission Overview

This laboratory activity focuses on improving the security of an Ubuntu server using UFW (Uncomplicated Firewall). I deployed an Nginx web application through Docker, tested its response, and configured firewall rules to manage incoming network traffic. The main goal was to apply a Default Deny policy while allowing only the necessary connections for SSH access and the web application. This activity demonstrated how proper firewall configuration helps reduce the server's attack surface and improve security.

## 🎯 Objectives

- Understand the Principle of Least Privilege and its role in cloud security.
- Identify the attack surface of a virtual machine and learn how to reduce unnecessary exposure.
- Configure UFW using a Default Deny policy for incoming connections.
- Allow SSH access and TCP port 8080 for the web application.
- Verify the firewall status and review the configured security rules.
- Record the commands, results, and screenshots using Markdown documentation.

## 💻 Commands Executed

### 1. Deploy and Test Nginx

```bash
docker run -d --name secure-web-app -p 8080:80 nginx
curl http://localhost:8080
```

These commands deploy the Nginx container and test whether the web server responds successfully.

### 2. Configure UFW

```bash
sudo ufw allow ssh
sudo ufw default deny incoming
sudo ufw default allow outgoing
sudo ufw enable
sudo ufw status verbose
```

These commands allow SSH connections, block incoming traffic by default, permit outgoing connections, activate the firewall, and display its current configuration.

### 3. Allow and Verify Web Traffic

```bash
sudo ufw allow 8080/tcp
sudo ufw status numbered
curl http://localhost:8080
```

These commands allow incoming TCP traffic through port 8080, display the numbered firewall rules, and test the Nginx web application again.

## 🛠️ Skills Learned

- Deploying and testing an Nginx web server using Docker.
- Configuring a Linux host-based firewall with UFW.
- Managing network ports and controlling incoming connections.
- Applying basic cloud security principles, including Least Privilege and Default Deny.
- Verifying firewall settings and application connectivity through terminal commands.
- Creating organized technical documentation using Markdown.
- Recording practical results through screenshots for a GitHub portfolio.

## 📸 Screenshots

The following screenshots provide evidence of the deployment and firewall configuration:

- `screenshots/vulnerable-app-running.png` — Shows the Nginx web application responding to a request.
- `screenshots/firewall-activated.png` — Shows the active UFW firewall and its default policies.
- `screenshots/firewall-port-allowed.png` — Shows the allowed firewall rules and the successful web application test.

## 📊 Mission Status

**In Progress** — The mission will be marked as completed after all required commands have been executed, screenshots have been uploaded, documentation has been finalized, and the changes have been committed to GitHub.

## ✅ Conclusion

This activity helped me understand that deploying a web application is only one part of managing a secure cloud server. Proper firewall configuration is also necessary to control network access and prevent unnecessary exposure. By allowing only the required connections and checking the firewall rules, I learned how to apply basic security measures to a Linux environment. These skills provide a useful foundation for managing and securing cloud-based applications.
