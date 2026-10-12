# System Baseline Report

## Checkpoint 2: Host System Baseline

### 1. Memory Assessment

**Command used:** `free -h`

The command showed that the server had approximately 1.9 GiB of total RAM.

* **Total RAM:** 1.9 GiB
* **Used RAM:** 404 MiB
* **Free RAM:** 1.2 GiB
* **Available RAM:** 1.5 GiB
* **Total Swap:** 1.0 GiB
* **Used Swap:** 0 B

During the check, the server had 1.5 GiB of available memory, meaning it still had memory that could be used by other tasks.

**Screenshot Evidence — Memory Check**

<img width="801" height="286" alt="Screenshot 2026-10-12 164719" src="https://github.com/user-attachments/assets/b1095fe4-428b-4521-9218-3a1e0d54e64d" />


### 2. Disk Assessment

**Command used:** `df -h /`

* **Total root filesystem capacity:** 19G
* **Used disk space:** 5.5G
* **Available disk space:** 13G
* **Disk usage:** 30%

The server had 13G of free disk space during the assessment. Checking storage before an increase in traffic is important because application data, logs, and temporary files can use up disk space and affect the service.

**Screenshot Evidence — Disk Usage Check**

<img width="801" height="286" alt="Screenshot 2026-10-12 164719" src="https://github.com/user-attachments/assets/bf5ceeb6-36b4-497e-a1f2-c84ce03842a4" />


### 3. CPU and Process Assessment

**Command used:** `top`

The `top` command was used to view active processes and check CPU and memory activity. It helped provide an overview of the server's condition during the baseline assessment.

The command was executed for approximately five seconds, as instructed in the laboratory activity. The exact CPU percentages and process counts were not recorded.

These results would help establish the server's initial condition before deploying the Nginx container and testing HTTP requests.

**Screenshot Evidence — CPU and Process Check**

<img width="1438" height="770" alt="image" src="https://github.com/user-attachments/assets/cf2b130e-12da-4d9c-8298-0baab4608cb6" />


### 4. Baseline Conclusion

The initial assessment showed that the server had 1.5 GiB of available memory and 13G of available disk space. The `top` command was also used to observe running processes and CPU activity. These checks provided basic information about the host before monitoring the Nginx container and its resource usage.

