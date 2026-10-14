# 🔐 Mission 8: The Cloud Security Engineer

## 📝 Checkpoint 7 – Mission Reflection

### Q1. How does a host-based firewall protect a server even if the physical network perimeter is breached?

**Answer:**

A host-based firewall protects a server by monitoring and controlling the network traffic that reaches the machine. Even if an attacker gets past the main network firewall, UFW can still block connections that are not allowed by its rules. This provides an extra layer of security for the server.

### Q2. Why is managing open network ports critical to reducing a server's attack surface?

**Answer:**

Managing open ports is important because unnecessary ports can give attackers more opportunities to access services on a server. Allowing only the ports needed for specific tasks helps reduce security risks and unwanted connections. In this mission, SSH and TCP port 8080 were allowed because they were needed for server management and web access.

### Q3. In a real enterprise environment, why is it dangerous to leave a database port like 3306 for MySQL open to the public internet?

**Answer:**

Leaving MySQL port 3306 open to the public internet can expose the database to unauthorized access attempts and possible attacks. If an attacker gets access, sensitive information could be stolen, modified, or deleted. To improve security, the database should accept connections only from trusted servers or authorized networks.

### Q4. How did completing this mission change your perspective on how easily a server can be compromised?

**Answer:**

This mission helped me understand that a server can become vulnerable if its security settings are not properly configured. Before, I mostly focused on making applications work, but now I understand that protecting access is equally important. I also learned that incorrect firewall settings can create security risks or prevent remote access. That is why firewall rules must be configured carefully and checked regularly.

### Q5. How does your GitHub portfolio currently look with eight completed missions?

**Answer:**

My GitHub portfolio now contains eight cloud computing missions that show my progress from learning basic cloud concepts to securing a server. Through these activities, I have gained practical experience with Linux, containers, storage, deployment, monitoring, and firewall configuration. I have also improved my ability to organize project files and document my work. This portfolio can help demonstrate my skills and serve as a reference for future IT projects and job opportunities.

## 🎯 Conclusion

Completing Mission 8 taught me that cloud security involves more than just running applications and making them accessible. It is also important to control network connections, limit unnecessary access, and check whether firewall rules are working properly. I can apply these lessons to my future cloud computing activities while continuing to improve my GitHub portfolio.
