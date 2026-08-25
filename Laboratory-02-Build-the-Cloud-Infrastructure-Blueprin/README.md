# ☁️ Cloud Infrastructure Blueprint

## 🎯 Mission Overview

This laboratory activity was designed to build a fundamental understanding of **cloud infrastructure** and the essential components that support it. Through the use of the **KillerCoda Playground** and **Linux Terminal**, I explored a cloud-based Linux environment, analyzed its system resources, identified key infrastructure components, and examined the services provided by leading cloud providers.

As part of the activity, I created a basic cloud infrastructure architecture for a fictional organization called **ARK**. The architecture demonstrates the relationship between users, the Internet, networking, computing resources, and storage within a cloud environment.

The laboratory also allowed me to gain hands-on experience with **technical documentation, Markdown, Git, and GitHub repository management**.

---

## 🎯 Objectives

The main objectives of this laboratory activity were to:

* ☁️ Describe the essential components that make up cloud infrastructure.
* 🖥️ Examine the hardware and software resources available within a Linux environment.
* 💾 Distinguish between compute, storage, networking, and identity resources.
* 🔗 Understand how cloud infrastructure components communicate and operate together.
* 📝 Develop professional technical documentation using Markdown.
* 🐙 Enhance and maintain a structured GitHub Cloud Computing portfolio.

---

## 🧩 Cloud Infrastructure Components

The fictional company **ARK** utilizes a basic cloud infrastructure composed of a user, Internet connection, network, compute resource, and storage resource.

| **🔧 Component**           | **📖 Description**                                                                              |
| -------------------------- | ----------------------------------------------------------------------------------------------- |
| 🖥️ **Compute Resource**   | Supplies the processing capability needed to execute applications, services, and workloads.     |
| 💾 **Storage Resource**    | Provides capacity for saving files, databases, application information, and other digital data. |
| 🌐 **Network**             | Establishes communication between cloud resources, users, applications, and services.           |
| 👤 **User**                | Represents a person or client who accesses and interacts with cloud-based resources.            |
| 🌍 **Internet Connection** | Enables users to connect to and communicate with cloud infrastructure over the Internet.        |

### 🏗️ Basic Architecture

The proposed infrastructure follows this general communication flow:

```text
        👤 USER
           │
           ▼
      🌐 INTERNET
           │
           ▼
     ☁️ CLOUD NETWORK
        (VPC/VNet)
        ┌────┴────┐
        ▼         ▼
   🖥️ COMPUTE   💾 STORAGE
```

This architecture illustrates how users reach cloud resources through the Internet and a cloud network. The **compute resource** is responsible for processing applications and workloads, while the **storage resource** maintains the data and information required by those applications.

---

## 🛠️ Tools and Technologies Used

Several tools and technologies were used to complete the different tasks in this laboratory activity:

| **🛠️ Tool / Technology**    | **📌 Purpose**                                                                            |
| ---------------------------- | ----------------------------------------------------------------------------------------- |
| 🎨 **Canva**                 | Used to create and visualize the cloud infrastructure architecture diagram.               |
| ☁️ **KillerCoda Playground** | Provided a browser-based Linux environment for performing cloud infrastructure exercises. |
| 💻 **Linux Terminal**        | Used to execute commands and examine system and network resources.                        |
| 🐙 **GitHub**                | Used to organize, manage, version, and publish the laboratory outputs.                    |
| 📝 **Markdown**              | Used to structure and present the laboratory documentation professionally.                |
| 🌐 **Web Browser**           | Used to access GitHub, cloud provider documentation, and other technical references.      |

---

## 💻 Linux Commands Executed

The following Linux commands were executed to examine the cloud-based environment and collect important system information.

| **💻 Command**               | **📖 Purpose**                                                                           |
| ---------------------------- | ---------------------------------------------------------------------------------------- |
| `cat /etc/os-release`        | Shows details about the installed Linux distribution and operating system.               |
| `uname -r`                   | Displays the version of the currently running Linux kernel.                              |
| `lscpu \| grep "Model name"` | Identifies the processor or CPU model installed in the system.                           |
| `lscpu \| grep "^CPU(s):"`   | Shows the number of available CPU processing units.                                      |
| `free -h`                    | Displays memory usage and availability in an easy-to-read format.                        |
| `df -h`                      | Shows disk capacity, used space, available space, and mounted storage.                   |
| `findmnt`                    | Lists mounted file systems and their associated mount points.                            |
| `hostname`                   | Displays the hostname assigned to the Linux machine.                                     |
| `hostname -I`                | Displays the IP address assigned to the system.                                          |
| `ip addr`                    | Provides information about network interfaces, IP addresses, and network configurations. |

### ⚡ Quick System Information Command

The following command combines several Linux utilities to gather essential system information efficiently:

```bash
echo "=== OPERATING SYSTEM ==="; cat /etc/os-release; \
echo "=== KERNEL ==="; uname -r; \
echo "=== CPU ==="; lscpu | grep "Model name"; \
echo "=== CPU CORES ==="; lscpu | grep "^CPU(s):"; \
echo "=== RAM ==="; free -h; \
echo "=== DISK ==="; df -h; \
echo "=== MOUNTED FILE SYSTEMS ==="; findmnt; \
echo "=== HOSTNAME ==="; hostname; \
echo "=== IP ADDRESS ==="; hostname -I
```

This combined command allows multiple system details to be collected in one execution, making the process of investigating a cloud-based Linux environment faster and more organized.

---

## 🧠 Skills and Knowledge Acquired

After completing this laboratory activity, I developed and improved several technical skills, including:

* ☁️ Recognizing the core components of cloud infrastructure.
* 💻 Using Linux terminal commands to examine server resources.
* 🖥️ Understanding how compute resources support cloud applications and workloads.
* 💾 Learning the role and importance of storage in cloud environments.
* 🌐 Understanding how networking enables communication between cloud resources.
* 🏗️ Creating a basic representation of a cloud infrastructure architecture.
* 📝 Producing organized and professional technical documentation with Markdown.
* 🐙 Managing files and projects using Git and GitHub.
* 🔎 Comparing infrastructure services offered by major cloud providers.
* 📂 Structuring laboratory activities and documentation within a GitHub repository.
* 🐧 Recognizing the importance of Linux as a fundamental technology in cloud computing.

---

## ⚠️ Challenges Encountered

One of the challenges I encountered was understanding how **compute, storage, networking, and Internet connectivity** interact with one another within a cloud environment. I also had to familiarize myself with several Linux commands used to examine system resources and configurations.

Another challenge was determining which information was most relevant when reviewing the documentation of **AWS, Microsoft Azure, and Google Cloud**, as each provider offers a wide range of infrastructure services.

Despite these challenges, the activity improved my confidence in working with **Linux environments, cloud infrastructure concepts, and technical documentation**.

---

## 🏁 Conclusion

This laboratory activity provided me with a clearer understanding of **cloud infrastructure and its fundamental components**. I learned how compute, storage, and networking resources interact to support cloud-based services and how Linux commands can be used to inspect and analyze system resources.

The activity also strengthened my practical skills in **Linux, cloud architecture, Markdown, Git, and GitHub**, which are valuable tools and technologies for future cloud computing activities.

> 💡 **Key Takeaway:** Cloud computing brings together **compute, storage, and networking resources** to deliver scalable services and resources that users can access through the Internet.

