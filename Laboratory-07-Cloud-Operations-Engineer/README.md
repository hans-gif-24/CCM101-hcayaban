# Laboratory Activity 7: The Cloud Operations Engineer

## Mission Overview

This activity is about checking the condition and performance of a Linux system and a web application running in Docker. Using KillerCoda and Docker, I checked the system resources, started an Nginx web server, tested HTTP requests, reviewed logs, and monitored the container's resource usage.

## Objectives

* Monitor the system's memory and disk space.
* Check CPU usage and active processes.
* Run an Nginx container.
* Test working and missing web pages.
* Review Docker logs and resource usage.
* Record the activity results in Markdown files.

## Monitoring Commands Executed

| **Command**                                            | **Purpose**                                        |
| ------------------------------------------------------ | -------------------------------------------------- |
| `free -h`                                              | View the system's memory usage                     |
| `df -h /`                                              | Check the storage capacity of the root filesystem  |
| `top`                                                  | View running processes and CPU activity            |
| `docker ps`                                            | View active Docker containers                      |
| `docker run -d --name client-website -p 8080:80 nginx` | Start the Nginx web server in the background       |
| `curl http://localhost:8080`                           | Check if the website is accessible                 |
| `curl http://localhost:8080/hidden-admin-page`         | Check the response from a page that does not exist |
| `docker logs client-website`                           | View the container's logs                          |
| `docker stats`                                         | Check the container's resource consumption         |

## Skills Learned

* Monitoring Linux resources
* Running Docker containers
* Testing HTTP responses
* Checking application logs
* Tracking container performance
* Writing technical documentation in Markdown

## Conclusion

Through this activity, I learned that running a cloud application is not only about making the service work. It is also important to monitor system resources, review logs, and check container performance. These tasks help identify errors and make troubleshooting easier.

## Evidence

Screenshots showing the results of the laboratory checkpoints are saved in the `screenshots` folder.

