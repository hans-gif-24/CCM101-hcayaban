# Mission 7 Reflection: The Cloud Operations Engineer

## 1. Why should we check the host server's resources even when containers are working properly?

We need to monitor the host server because containers rely on the resources available on the machine. Even if an application works well, low memory, high CPU usage, or limited disk space can affect its performance. Checking these resources helps us find possible problems before they affect the service.

## 2. How can `docker logs` help when a user cannot log in?

I would use `docker logs` to review the activities and errors recorded by the application container. It may show failed requests or server problems related to the login issue. If another service handles authentication, I would also check its logs to get more information.

## 3. What is the difference between logs and metrics monitoring?

Logs contain records of specific events, such as a request that receives a 404 error. Metrics show numerical data like CPU usage, memory consumption, and network activity. Logs help us understand what happened, while metrics help us monitor the system's performance.

## 4. How do large companies monitor thousands of containers?

Large companies use monitoring tools to gather information from different containers and servers. Prometheus collects performance metrics, while Grafana displays the data through dashboards and graphs. Alerting tools can also notify the operations team when a problem or unusual resource usage occurs.

## 5. How did your troubleshooting skills in Linux improve?

My troubleshooting skills improved because I learned to check system information before identifying a possible problem. I practiced monitoring memory and disk space, running an Nginx container, testing HTTP requests, checking logs, and viewing Docker statistics. I also learned that applications need continuous monitoring even when they are working properly.

## Overall Reflection

Mission 7 helped me understand that cloud operations is not just about running an application. It also involves checking system resources, reviewing logs, and monitoring performance to identify possible issues. These activities helped me become more familiar with troubleshooting and understand how monitoring supports a reliable cloud service.

