# 🏗️ Multi-Tier Architecture

## 📖 What Is a Two-Tier Architecture?

A two-tier architecture is a system design that divides an application into two main components: the **web/application tier** and the **database tier**. Each component performs a different task, but both work together to provide the complete service.

In this laboratory activity, Nextcloud serves as the web application, while MariaDB manages the database information required by the system. Separating these components helps organize the application and makes each service easier to manage.

## 1. 🌐 Web/Application Tier

The web/application tier is the part of the system that users access through their web browsers. In this project, **Nextcloud** provides the interface where users can access and manage their files.

It receives requests from users, displays web pages, and communicates with the database whenever information needs to be retrieved or updated. This tier handles the main application functions and allows users to interact with the system.

## 2. 🗄️ Database Tier

The database tier is responsible for storing and managing the information used by the application. In this activity, **MariaDB** serves as the database for Nextcloud.

It stores application records, including user information and other data needed to manage files. When Nextcloud needs to save or retrieve information, it communicates with MariaDB to perform the required database operations.

## 3. 💡 Why Separate the Two Tiers?

Separating Nextcloud and MariaDB into different containers makes the application more organized and easier to maintain. Each service can be configured, monitored, and updated independently, which also makes troubleshooting more manageable.

This design also provides flexibility for future improvements. For example, the application and database resources can be adjusted separately as the system grows. However, proper networking, security, and backup configurations are still necessary to keep the services reliable.

## 🔄 Architecture Flow

The application follows this communication process:

**User's Browser → Nextcloud Application Container → MariaDB Database Container**

1. The user opens Nextcloud through a web browser using port `8080`.
2. Docker maps host port `8080` to port `80` inside the Nextcloud application container.
3. Nextcloud processes the user's requests and communicates with MariaDB when database information is needed.
4. The database service is identified by the name `database` through the Docker Compose network.
5. Nextcloud uses the database results to complete the requested operation and display the appropriate response to the user.

## 📝 Conclusion

This activity helped me understand how a two-tier architecture separates an application into two connected components. Nextcloud handles the user interface and application functions, while MariaDB stores the information required by the system.

By deploying these services in separate Docker containers, I learned how application and database components communicate within a shared environment. This architecture provides a useful foundation for understanding how modern web applications are organized, deployed, and maintained in cloud environments.

