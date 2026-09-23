# AWS S3 Static Website Hosting

## 📌 Project Description

This project demonstrates the use of **Amazon S3** to host a static website and implement basic **data lifecycle management** and **disaster recovery (DR)** strategies.

The project focuses on practical AWS S3 concepts including **static website hosting, lifecycle policies, versioning, data protection, and recovery**.

---

## 🏗️ Architecture

```text
                         Internet
                            │
                            ▼
                    ┌───────────────┐
                    │   Amazon S3   │
                    │    Bucket     │
                    └───────┬───────┘
                            │
             ┌──────────────┼──────────────┐
             │              │              │
             ▼              ▼              ▼
      Static Website   Lifecycle       Disaster
         Hosting       Management      Recovery
                            │              │
                            ▼              ▼
                       Object        Versioning &
                       Lifecycle     Object Recovery
```

---

## 🎯 Objectives

### 1. Host a static website using Amazon S3

Configured an Amazon S3 bucket to host a static website containing HTML, CSS, and other static assets. with versioning enabled to revcover from accedental deletes

**Screenshot:**

![S3 Static Website Hosting](screenshots/createnupload.png)
The website
![S3 Static Website Hosting](screenshots/thewebsite.png)


---
### 2. implement versioning 

to protect from accedental deletes and to roll back to previous versions of a website if the update is not optimal for example
uploaded new versionof website
![S3 Static Website Hosting](screenshots/versioning1.png)
the new version
![S3 Static Website Hosting](screenshots/newversion.png)
versions in the version tab of an object index.html
![S3 Static Website Hosting](screenshots/versioning2.png)

i decided to roll back to the original copy by downloading the old version and uploading it again
![S3 Static Website Hosting](screenshots/versioning2.png)





### 2. Implement a data lifecycle strategy in Amazon S3

Configured an **S3 Lifecycle Rule** to automatically manage objects according to their lifecycle and optimize storage management.

created a lifecycle to transistion versions of objects to S3-standared-IA
![S3 Lifecycle Configuration](screenshots/lifecycle1.png)
![S3 Lifecycle Configuration](screenshots/lifecycle11.png)
created a lifecycle to delete noncurrent objects 
![S3 Lifecycle Configuration](screenshots/lifecycle2.png)
all the lifecycle policies
![S3 Lifecycle Configuration](screenshots/lifecycle3.png)




---

### 3. Implement a disaster recovery (DR) strategy in Amazon S3

Enabled **S3 Versioning** in both s3 buckets source and destination 
create the DR bucket in another region
![S3 Versioning and Recovery](./screenshots/drbucket.png)
DR bucket with objects newly uploaded to the source so they are replicated here 
![S3 Lifecycle Configuration](screenshots/dr.png)
