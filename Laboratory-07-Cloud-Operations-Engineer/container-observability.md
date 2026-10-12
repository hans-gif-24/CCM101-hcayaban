# Container Observability Report

## Checkpoint 4: Application Logging

### Command Used

```bash
docker logs client-website
```

This command showed the startup information and HTTP request records from the Nginx container named `client-website`.

### 404 Error Log

```text
2026/10/12 08:53:39 [error] 29#29: *4 open() "/usr/share/nginx/html/hidden-admin-page" failed (2: No such file or directory), client: 172.17.0.1, server: localhost, request: "GET /hidden-admin-page HTTP/1.1", host: "localhost:8080"
172.17.0.1 - - [12/Oct/2026:08:53:39 +0000] "GET /hidden-admin-page HTTP/1.1" 404 153 "-" "curl/8.5.0" "-"
```

### Log Analysis

The log indicates that someone requested `/hidden-admin-page`, but Nginx returned a `404` response because the requested page was not found. This shows how logs can help administrators identify missing pages and investigate website problems.

### Why Application Logs Are Important

Application logs keep records of website requests and errors while a service is running. They help administrators understand what happened by providing details such as the requested URL, time, and HTTP status code.

### Screenshot Evidence

Save your Docker logs screenshot in the `screenshots` folder as `docker-logs.png`.

## Checkpoint 5: Real-Time Container Metrics

### Command Used

```bash
docker stats
```

### Observed Container Metrics

| **Metric**              | **Actual Result** |
| ----------------------- | ----------------- |
| Container Name          | `client-website`  |
| Container ID            | `6aa25414c87c`    |
| CPU Usage               | 0.00%             |
| Memory Usage            | 2.738 MiB         |
| Memory Limit            | 1.859 GiB         |
| Memory Usage Percentage | 0.14%             |
| Network I/O             | 3.77 kB / 5.29 kB |
| Block I/O               | 0B / 12.3 kB      |
| Processes (PIDS)        | 2                 |

### Analysis

During monitoring, the `client-website` container used 0.00% CPU and 2.738 MiB of memory. Its memory usage was only 0.14% of the displayed limit, showing that Nginx was using a small amount of resources at that time.

The network and block I/O values also recorded the container's network transfers and disk activity. However, these readings only show the container's resource usage during the test and do not guarantee that it can support thousands of users at once.

### Screenshot Evidence — Real-Time Container Metrics

<img width="1332" height="188" alt="image" src="https://github.com/user-attachments/assets/9653bb6b-1fca-4f55-a504-4e7531054324" />

