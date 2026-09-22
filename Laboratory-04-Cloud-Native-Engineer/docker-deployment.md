# ☁️ Checkpoint 5 - The Container Lifecycle

This document discusses the basic Docker commands for managing containers, such as checking running containers, stopping them, confirming their status, and deleting them.

## Container Lifecycle Commands

### 1. List Running Containers

**Command:**

```bash
docker ps
```

**What it does:** Shows all active containers and their details, including the container ID, image, command, status, ports, and name. This helps identify which containers are currently running.

**Terminal Output:**

```text
CONTAINER ID   IMAGE   COMMAND                  STATUS   PORTS                  NAMES
xxxxxxxxxxxx   nginx   "/docker-entrypoint..."  Up       0.0.0.0:8080->80/tcp   my-nginx
```

The result shows that the **`my-nginx`** container is currently running.

💡 **Tip:** Use `docker ps -a` to see all containers, including those that are stopped.

---

### 2. Stop the Running Container

**Command:**

```bash
docker stop my-nginx
```

**What it does:** Stops the selected container properly by giving the application time to shut down before it terminates.

**Terminal Output:**

```text
my-nginx
```

The output indicates that the **`my-nginx`** container has been stopped successfully.

---

### 3. Check If the Container Has Stopped

**Command:**

```bash
docker ps -a
```

**What it does:** Displays all containers so I can check whether `my-nginx` has stopped. Its status should show **Exited (0)** if it stopped successfully.

**Terminal Output:**

```text
CONTAINER ID   IMAGE   COMMAND                  STATUS          PORTS   NAMES
xxxxxxxxxxxx   nginx   "/docker-entrypoint..."  Exited (0) ...          my-nginx
```

The **Exited (0)** status indicates that the container finished running successfully.

💡 **Tip:** The `docker ps` command only shows running containers, so stopped containers will not appear unless I use `-a`.

---

### 4. Delete the Container

**Command:**

```bash
docker rm my-nginx
```

**What it does:** Deletes the stopped `my-nginx` container from Docker, including its container information and writable layer.

**Terminal Output:**

```text
my-nginx
```

The output confirms that the container has been removed.

To check if the container was completely deleted, I used:

```bash
docker ps -a
```

**Terminal Output:**

```text
CONTAINER ID   IMAGE   COMMAND   CREATED   STATUS   PORTS   NAMES
```

The empty list confirms that **`my-nginx` has been completely removed** from the system.

---

## 📝 Summary

| # | Command                | Purpose                     | Result                              |
| - | ---------------------- | --------------------------- | ----------------------------------- |
| 1 | `docker ps`            | Display running containers  | `my-nginx` appears as **Up**        |
| 2 | `docker stop my-nginx` | Stop the container properly | Container stopped                   |
| 3 | `docker ps -a`         | Check the container status  | Status shows **Exited (0)**         |
| 4 | `docker rm my-nginx`   | Delete the container        | Container removed and list is empty |

Understanding the Docker container lifecycle is an important skill for a **Cloud-Native Engineer**. These four commands help me manage containers through a simple process: **list → stop → verify → remove**.
