# 🔐 Security Audit Report

## Mission 8: The Cloud Security Engineer

### 1. 🔑 Principle of Least Privilege (PoLP)

The Principle of Least Privilege means giving users, applications, and services only the permissions they need to perform their assigned tasks. In cloud computing, this helps prevent unauthorized access to important files, system resources, and services. By limiting permissions, administrators can reduce security risks and minimize the possible damage if an account or application is compromised. This principle helps maintain a more secure and controlled cloud environment.

### 2. 🎯 Attack Surface

The attack surface refers to all the possible entry points that an attacker could use to access or exploit a virtual machine. These may include open network ports, running services, remote access connections, and applications with security weaknesses. A larger attack surface can create more opportunities for unauthorized access. To reduce these risks, cloud administrators should disable unnecessary services, close unused ports, and allow only the connections required for normal operations.

### 3. 🛡️ Default Deny Policy

A Default Deny policy blocks incoming network connections unless they are specifically permitted by a firewall rule. This approach improves security because access is restricted by default rather than allowing connections and blocking them individually afterward. Administrators can create rules for trusted services while preventing unapproved traffic from reaching the server. This follows the principle of least privilege and helps reduce the risk of unauthorized network access.

### 📝 Initial Security Plan

Before applying the security settings, I will deploy and test the Nginx web application to confirm that it is running correctly and responding to requests. Next, I will configure UFW to deny incoming connections by default while allowing SSH for remote administration and TCP port 8080 for web application access. After enabling the firewall, I will review its status and verify that the required ports are allowed. I will also capture screenshots of the application and firewall rules to document the results of the activity.

### ✅ Audit Conclusion

This security audit focuses on reducing the server's attack surface while keeping essential services accessible. By applying the Default Deny policy and allowing only the necessary network connections, the server can be better protected against unauthorized access. Regularly reviewing firewall rules and checking active services are also important practices for maintaining a secure cloud environment. These measures demonstrate how proper firewall configuration supports the overall security and reliability of a cloud-based server.
