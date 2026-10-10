# ☁️ MinIO Object Storage Deployment

## 1. Project Overview

This activity demonstrates how to set up an S3-compatible object storage service using Docker. I used **MinIO** to create a simple cloud storage environment for a photo-sharing application. This setup allows user-uploaded images to be stored separately from the application's web server, making file management more organized.

## 2. Deployment Environment

The following tools and settings were used for the deployment:

* **Platform:** KillerCoda Ubuntu Playground
* **Container Tool:** Docker
* **Storage Service:** MinIO
* **API Port:** 9000
* **Web Console Port:** 9001
* **Container Name:** `minio-server`
* **Bucket Name:** `client-photos`

## 3. Docker Deployment Command

I used the following command to create and run the MinIO server container:

```bash
docker run -d \
  -p 9000:9000 \
  -p 9001:9001 \
  --name minio-server \
  -e "MINIO_ROOT_USER=cloudadmin" \
  -e "MINIO_ROOT_PASSWORD=CloudNova2026!" \
  minio/minio server /data \
  --console-address ":9001"
```

### Explanation of the Command

| **Command Option**           | **Purpose**                                                                             |
| ---------------------------- | --------------------------------------------------------------------------------------- |
| `-d`                         | Runs the container in the background.                                                   |
| `-p 9000:9000`               | Connects the host's port 9000 to the MinIO API port.                                    |
| `-p 9001:9001`               | Connects the host's port 9001 to the MinIO Web Console.                                 |
| `--name minio-server`        | Gives the container a specific name for easier management.                              |
| `-e MINIO_ROOT_USER=...`     | Sets the initial administrator username.                                                |
| `-e MINIO_ROOT_PASSWORD=...` | Sets the initial administrator password.                                                |
| `minio/minio`                | Identifies the MinIO Docker image to use.                                               |
| `server /data`               | Starts the MinIO server and uses `/data` as its storage directory inside the container. |
| `--console-address ":9001"`  | Sets port 9001 as the listening port for the Web Console.                               |

The `-e` option is used to provide environment variables to the container. In this setup, these variables configure the initial administrator login credentials for MinIO.

## 4. Accessing the Console and Creating a Bucket

After starting the container, I accessed the MinIO Web Console through port `9001` using the port-access feature provided by KillerCoda.

Once I reached the login page, I signed in using the configured administrator credentials. I then created a bucket named `client-photos` and uploaded a sample file to test whether the object storage service was working correctly.

A **bucket** is a storage container used to organize objects, such as images, documents, and other files. For this activity, the `client-photos` bucket serves as the storage location for images uploaded by users of the photo-sharing application.

## 5. Deployment Verification

To check whether the MinIO container was running, I used the following Docker command:

```bash
docker ps
```

This command displays the currently running containers. If the deployment is successful, the `minio-server` container should appear in the output.

I also checked the MinIO Web Console to confirm that the `client-photos` bucket had been created and that the uploaded sample file was visible. These checks helped verify that the storage service was running and that the basic object storage operations were completed.

## 6. Security Considerations

For this classroom activity, I used the administrator credentials configured in the deployment command. However, real cloud deployments require stronger security practices to protect storage services and their data.

Administrator credentials should be strong, unique, and kept private. They should not be shared publicly or committed to a public GitHub repository. Access to the MinIO console should also be restricted to authorized users. For production environments, it is important to configure persistent storage, regular backups, monitoring, and appropriate network security controls.

## 7. Conclusion

This activity helped me understand how Docker can be used to deploy an object storage service with MinIO. I learned how to configure the container, map network ports, access the management console, create a bucket, and upload a sample object.

It also showed me how storage services can operate separately from web applications, providing a dedicated place to manage uploaded files. Overall, this laboratory improved my practical knowledge of **Docker, object storage, cloud deployment, and basic storage security**.

