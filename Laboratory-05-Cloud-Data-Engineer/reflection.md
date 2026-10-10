# 🤔 Mission 5 Reflection: The Cloud Data Engineer

## 1. Why is Object Storage more suitable for storing millions of photos than a traditional Block Storage hard drive?

Object Storage is more suitable for storing millions of photos because it organizes each file as an object with its own unique identifier and metadata. It can handle large amounts of unstructured data and can scale as more photos are uploaded. Block Storage is commonly used for operating systems and databases, while Object Storage is a practical choice for applications that need to store and manage many images.

## 2. How did Docker make deploying the MinIO storage server easier?

Docker made the deployment process simpler because I could start the MinIO server using a single command instead of installing and configuring everything manually. I also learned how to set environment variables and map network ports to make the service accessible. This activity helped me understand how Docker can simplify the deployment and management of cloud services.

## 3. What is a bucket in cloud storage?

A bucket is a storage container used to organize and store objects in an object storage system. In this activity, I created a bucket called `client-photos` in MinIO. It serves as the storage location for the sample files uploaded during the exercise. I learned that buckets help keep stored data organized and easier to manage.

## 4. How do large enterprise companies protect their object storage data if a physical server fails?

Large companies protect their data by keeping multiple copies on different disks or servers and using replication and regular backups. They may also enable versioning to recover earlier versions of files when needed. Monitoring systems can help detect storage problems before they cause bigger issues. These practices help reduce the risk of permanent data loss when hardware fails.

## 5. How is your confidence in using the Linux command line improving?

My confidence in using the Linux command line has improved because I can now execute Docker commands, check running containers, and understand basic error messages. During this activity, I experienced difficulties downloading the original MinIO image, so I had to troubleshoot the problem and try an alternative image source. This experience taught me the importance of patience, problem-solving, and understanding errors when working with cloud technologies.

## 📝 Overall Reflection

Overall, this laboratory gave me a better understanding of object storage and its role in cloud computing. I gained hands-on experience deploying MinIO with Docker, creating a bucket, uploading files, and checking whether the storage service was working correctly.

I also realized that becoming a cloud engineer requires more than knowing commands. It involves understanding how services work, solving technical problems, and following good security practices. This activity helped me improve my technical skills and gave me more confidence in working with Linux, Docker, and cloud storage systems.

