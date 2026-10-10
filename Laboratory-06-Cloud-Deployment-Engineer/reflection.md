# ☁️ Mission 6 Reflection: The Cloud Deployment Engineer

## Question and Answer

### 1. How does writing a `docker-compose.yml` file make a cloud engineer's job easier compared to manually typing commands?

**Answer:** Using a `docker-compose.yml` file makes deployment easier because the settings for all services are stored in one file. Instead of running commands one by one, I can use a single command to start the application and database. It also helps make the deployment process more organized and repeatable.

### 2. What happens if you make an indentation error, like using a Tab instead of Spaces, in a YAML file?

**Answer:** An indentation error may cause Docker Compose to display an error or read the configuration incorrectly. YAML uses spaces to organize its settings, so proper alignment is important. I learned that checking the indentation carefully can help avoid deployment problems.

### 3. Why did we use environment variables like `MYSQL_PASSWORD` in the Compose file?

**Answer:** Environment variables provide the settings needed for containers to communicate and work correctly. In this activity, they define database details such as the username, password, database name, and hostname. I also learned that passwords should be stored securely when working with real applications.

### 4. How did it feel to deploy a fully functional enterprise cloud storage system (Nextcloud) in just a few minutes?

**Answer:** I felt happy and excited because I was able to deploy a cloud storage application using Docker Compose. It was interesting to see Nextcloud and MariaDB work together using separate containers. This activity showed me how automation can make application deployment faster and easier.

### 5. How has your understanding of Cloud Computing evolved since Mission 1?

**Answer:** Since Mission 1, I have learned more about cloud infrastructure, cloud platforms, containers, storage, and application deployment. I now understand that cloud computing is not only about using online services but also about configuring, testing, and managing the systems behind them. Proper planning and documentation are also important for reliable applications.

## Overall Reflection

This mission helped me understand Docker Compose and Infrastructure as Code better. I learned how to configure services using a YAML file, connect an application to a database, and manage containers through simple commands. I also realized that even small configuration errors can affect the entire deployment process.

Compared with my first laboratory activity, I am now more comfortable using the Linux terminal and organizing my activities in GitHub. Although I still need more practice, this experience has improved my confidence in deploying applications that use multiple containers. I can use what I learned as a starting point for studying more advanced cloud deployment techniques in the future.

