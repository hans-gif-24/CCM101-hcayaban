# 🐧 Checkpoint 7 – Linux Investigation and Cloud Migration

## Overview

This checkpoint focuses on examining the specifications of a Linux server running in the **KillerCoda Ubuntu Playground**. The goal is to identify the server's resources and determine which major cloud platforms can provide similar resources and support the same Linux environment.

---

# 🖥️ 1. Linux Server Specifications

The information below was collected from the **KillerCoda Ubuntu Playground**. The environment uses a virtualized **Ubuntu 24.04.4 LTS** server with basic computing resources.

| **Specification**       | **Details**                                   |
| ----------------------- | --------------------------------------------- |
| 🐧 **Operating System** | Ubuntu 24.04.4 LTS (Noble Numbat)             |
| 📦 **Distribution**     | Ubuntu                                        |
| 🔢 **Version**          | 24.04                                         |
| 🏗️ **Architecture**    | x86_64                                        |
| ⚙️ **CPU**              | 1 CPU                                         |
| 🧩 **CPU Model**        | Intel Xeon E312xx (Sandy Bridge, IBRS update) |
| 🚀 **CPU Speed**        | 2.0 GHz                                       |
| 🔹 **CPU Cores**        | 1 Core                                        |
| 🧵 **CPU Threads**      | 1 Thread                                      |
| ☁️ **Hypervisor**       | KVM                                           |
| 💻 **Virtualization**   | Full Virtualization                           |
| 🧠 **RAM**              | 1.9 GiB                                       |
| 📊 **RAM Used**         | 417 MiB                                       |
| 🟢 **RAM Available**    | 1.5 GiB                                       |
| 🔄 **Swap Memory**      | 1.0 GiB                                       |
| 💾 **Disk Capacity**    | 19 GB                                         |
| 📈 **Disk Used**        | 5.4 GB                                        |
| 🟢 **Disk Available**   | 13 GB                                         |
| 📊 **Disk Usage**       | 30%                                           |

### 🔎 Server Summary

The KillerCoda environment is a small virtual machine with **1 CPU, 1.9 GiB of RAM, and 19 GB of storage**. These specifications give us an idea of the minimum resources needed to create a similar Linux virtual machine in a cloud environment.

---

# ☁️ 2. Cloud Services That Can Host the Server

The KillerCoda environment is a **virtualized Ubuntu 24.04.4 LTS server**. Since AWS, Microsoft Azure, and Google Cloud Platform all provide virtual machines that support Linux, this server can be recreated on any of these three cloud platforms.

---

## 🟧 AWS – Amazon EC2

### Amazon Elastic Compute Cloud (EC2)

| **Item**                   | **Details**                                                                                                                                                                                                                       |
| -------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| ☁️ **Cloud Service**       | **Amazon EC2 (Elastic Compute Cloud)**                                                                                                                                                                                            |
| ✅ **Can Host the Server?** | **Yes**                                                                                                                                                                                                                           |
| 💡 **Reason**              | Amazon EC2 supports Linux distributions such as Ubuntu. A small EC2 instance can provide CPU and memory resources similar to the KillerCoda server. Additional storage can also be configured to meet the required 19 GB or more. |
| 🎯 **Suitable For**        | Ubuntu servers, websites, applications, development environments, and other Linux workloads.                                                                                                                                      |
| 🏁 **Conclusion**          | **Amazon EC2 can host a similar Ubuntu server environment.**                                                                                                                                                                      |

---

## 🔵 Microsoft Azure – Azure Virtual Machines

### Azure Virtual Machines

| **Item**                   | **Details**                                                                                                                                                                                      |
| -------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| ☁️ **Cloud Service**       | **Azure Virtual Machines**                                                                                                                                                                       |
| ✅ **Can Host the Server?** | **Yes**                                                                                                                                                                                          |
| 💡 **Reason**              | Azure Virtual Machines supports Ubuntu and other Linux distributions. Users can select a suitable VM size for the required CPU and memory, while Azure managed disks can provide enough storage. |
| 🎯 **Suitable For**        | Ubuntu servers, websites, web applications, development environments, and Linux-based services.                                                                                                  |
| 🏁 **Conclusion**          | **Azure Virtual Machines can host a similar Ubuntu server environment.**                                                                                                                         |

---

## 🔴 GCP – Google Compute Engine

### Google Compute Engine

| **Item**                   | **Details**                                                                                                                                                                                                                 |
| -------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| ☁️ **Cloud Service**       | **Google Compute Engine**                                                                                                                                                                                                   |
| ✅ **Can Host the Server?** | **Yes**                                                                                                                                                                                                                     |
| 💡 **Reason**              | Google Compute Engine supports Ubuntu Linux and allows users to customize the resources of a virtual machine. The VM can be configured with enough CPU, RAM, and storage to meet the requirements of the KillerCoda server. |
| 🎯 **Suitable For**        | Ubuntu servers, websites, applications, development environments, and other Linux workloads.                                                                                                                                |
| 🏁 **Conclusion**          | **Google Compute Engine can host a similar Ubuntu server environment.**                                                                                                                                                     |

---

# 📊 3. Cloud Platform Comparison

The three major cloud providers can support the requirements of the KillerCoda Ubuntu server. Each provider offers virtual machine services where users can select the operating system and configure resources such as CPU, memory, and storage.

| **Cloud Provider**     | **Cloud Service**      | **Ubuntu Support** | **Can Match Server Requirements?** |
| ---------------------- | ---------------------- | ------------------ | ---------------------------------- |
| 🟧 **AWS**             | Amazon EC2             | ✅ Yes              | ✅ Yes                              |
| 🔵 **Microsoft Azure** | Azure Virtual Machines | ✅ Yes              | ✅ Yes                              |
| 🔴 **GCP**             | Google Compute Engine  | ✅ Yes              | ✅ Yes                              |

---

# 🏆 Final Conclusion

The **KillerCoda Ubuntu server can be recreated or migrated to any of the three major cloud platforms**. AWS, Azure, and GCP all offer virtual machine services that support Ubuntu Linux and allow users to provide the necessary computing resources.

### 🎯 Key Findings

* 🟧 **AWS EC2** → A good option for flexible and scalable Linux server deployments.
* 🔵 **Azure Virtual Machines** → A suitable choice for organizations that already use Microsoft technologies.
* 🔴 **Google Compute Engine** → A flexible option for customized Linux environments and development workloads.

> 💡 **Key Takeaway:** Moving a Linux environment to the cloud allows it to run on scalable virtual infrastructure instead of a temporary playground. The best platform depends on factors such as **cost, performance, existing technology, scalability, management needs, and organizational goals**.

