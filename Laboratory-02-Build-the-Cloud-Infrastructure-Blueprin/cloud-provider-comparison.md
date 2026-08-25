# ☁️ Checkpoint 4 – Major Cloud Provider Comparison

Cloud service providers deliver many of the same fundamental infrastructure capabilities, although their services often have different names, architectures, and implementation approaches. This comparison examines four essential infrastructure areas: **Compute, Storage, Networking, and Identity and Access Management (IAM)**.

The three major cloud platforms included in this comparison are:

* ☁️ **Amazon Web Services (AWS)**
* 🔷 **Microsoft Azure**
* 🌐 **Google Cloud Platform (GCP)**

---

## 📊 Cloud Provider Service Comparison

| **🏗️ Infrastructure Component**          | **☁️ Amazon Web Services (AWS)**                                                                               | **🔷 Microsoft Azure**                                                                                                                    | **🌐 Google Cloud Platform (GCP)**                                                                                            |
| ----------------------------------------- | -------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| **💻 Compute**                            | **Amazon EC2** – Offers scalable virtual servers for hosting applications, services, and workloads.            | **Azure Virtual Machines** – Provides scalable virtual machines capable of supporting Windows and Linux workloads.                        | **Compute Engine** – Provides configurable virtual machines designed for various computing requirements.                      |
| **💾 Storage**                            | **Amazon S3** – Provides object storage for applications, backups, files, and archival data.                   | **Azure Blob Storage** – Provides scalable object storage for large volumes of unstructured data.                                         | **Cloud Storage** – Offers secure and scalable object storage for applications and digital data.                              |
| **🌐 Networking**                         | **Amazon VPC** – Enables organizations to create isolated and customizable virtual networks for AWS resources. | **Azure Virtual Network (VNet)** – Provides private networking and communication between Azure resources and external networks.           | **Virtual Private Cloud (VPC)** – Provides networking capabilities for Compute Engine, GKE, and other Google Cloud workloads. |
| **🔐 Identity & Access Management (IAM)** | **AWS IAM** – Manages users, roles, authentication, authorization, and permissions for AWS resources.          | **Microsoft Entra ID + Azure RBAC** – Provides identity management and controls access to Azure resources through role-based permissions. | **Google Cloud IAM** – Manages access to Google Cloud resources using identities, roles, and permissions.                     |

### 🔎 Service Equivalents

| **📂 Category**     | **☁️ AWS** | **🔷 Azure**                    | **🌐 GCP**       |
| ------------------- | ---------- | ------------------------------- | ---------------- |
| **Compute**         | Amazon EC2 | Azure Virtual Machines          | Compute Engine   |
| **Object Storage**  | Amazon S3  | Azure Blob Storage              | Cloud Storage    |
| **Virtual Network** | Amazon VPC | Azure Virtual Network           | Google Cloud VPC |
| **IAM**             | AWS IAM    | Microsoft Entra ID / Azure RBAC | Google Cloud IAM |

AWS provides **Amazon EC2** for flexible and scalable computing, while **Amazon VPC** enables customizable networking environments. **AWS IAM** manages authentication, authorization, identities, and permissions across AWS resources.

Azure offers **Azure Virtual Machines** for virtualized Windows and Linux workloads and **Azure Virtual Network** for private communication between Azure resources, the Internet, and on-premises environments. **Microsoft Entra ID** handles identity management, while **Azure RBAC** manages resource-level permissions.

Google Cloud provides **Compute Engine** for virtual machine workloads, **Cloud Storage** for object-based data storage, and **VPC** for cloud networking. **Google Cloud IAM** uses roles and permissions to regulate access to cloud resources.

---

# 📝 Guide Questions

## 1. Which cloud provider offers the broadest range of services? Explain your answer.

**Amazon Web Services (AWS)** is commonly regarded as one of the cloud providers with the most extensive selections of services. Its offerings cover areas such as **computing, storage, networking, databases, analytics, security, artificial intelligence, machine learning, containers, and IoT**. This broad portfolio gives organizations numerous options for building and deploying different types of workloads.

## 2. Which cloud platform would you recommend for an organization that primarily uses Microsoft products? Why?

**Microsoft Azure** would be an appropriate choice for an organization that already relies heavily on Microsoft technologies. Azure provides strong integration with products and services such as **Microsoft 365, Windows Server, SQL Server, and Microsoft Entra ID**. This integration can make identity management, authentication, application deployment, and connection with existing Microsoft environments more convenient.

## 3. Which platform is widely recognized for Artificial Intelligence (AI), Machine Learning (ML), and Kubernetes services?

**Google Cloud Platform (GCP)** is well known for its capabilities in **Artificial Intelligence, Machine Learning, and Kubernetes**. It provides various AI and ML technologies, while **Google Kubernetes Engine (GKE)** offers a managed platform for deploying and operating containerized applications using Kubernetes.

## 4. What similarities did you observe among the three cloud providers?

The three cloud providers offer comparable core infrastructure services, particularly in **compute, storage, networking, and identity and access management**. Although their service names, architectures, and implementation methods vary, all three platforms provide scalable, secure, and highly available cloud resources.

These services allow organizations to deploy applications and workloads without having to own and maintain all of the underlying physical infrastructure.

---

# 📚 Official Documentation References

* **☁️ AWS Documentation** – [AWS Documentation](https://docs.aws.amazon.com/)
* **🔷 Microsoft Azure Documentation** – [Microsoft Learn – Azure](https://learn.microsoft.com/en-us/azure/)
* **🌐 Google Cloud Documentation** – [Google Cloud Documentation](https://cloud.google.com/docs)

---

## ✅ Conclusion

AWS, Azure, and GCP provide similar fundamental cloud infrastructure capabilities, but each platform differs in its **service names, architecture, features, and areas of specialization**. Learning the equivalent services across these platforms helps cloud engineers understand different cloud environments and choose an appropriate provider based on an organization's technical requirements.

> 💡 **Key Takeaway:** Although AWS, Azure, and GCP use different service names and technologies, they provide comparable solutions for **compute, storage, networking, and identity management**.

