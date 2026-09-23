# AWS S3 Static Website Hosting, Lifecycle Management & Disaster Recovery

## 📌 Project Description

A hands-on **Amazon S3** project demonstrating static website hosting, **data lifecycle management**, **data protection**, and a basic **disaster recovery (DR)** strategy.

The project focuses on practical AWS skills relevant to **Cloud Support Engineer** and **Junior Cloud Engineer** roles, including **S3 Versioning, Lifecycle Policies, Storage Classes, and Cross-Region Replication**.

---

## 🏗️ Architecture

```text
                         Users
                           │
                           ▼
                 ┌──────────────────┐
                 │   S3 Website     │
                 │  Source Bucket   │
                 │   Region A       │
                 └────────┬─────────┘
                          │
             ┌────────────┴────────────┐
             │                         │
             ▼                         ▼
      Lifecycle Rules             Versioning
             │                         │
             ▼                         ▼
      Storage Class              Data Recovery
      Management
             │
             │ Cross-Region Replication
             ▼
                 ┌──────────────────┐
                 │   S3 DR Bucket   │
                 │   Region B       │
                 └──────────────────┘
```

---

## 🎯 Objectives

### 1. Host a Static Website Using Amazon S3

Configured an **Amazon S3 bucket for static website hosting** and uploaded the website files and assets.

![S3 Website Bucket](./screenshots/createnupload.png)

### 🌐 Deployed Website

![Deployed Static Website](./screenshots/thewebsite.png)

---

### 2. Implement a Data Lifecycle Strategy in Amazon S3

Configured **S3 Lifecycle Rules** to automatically manage object versions and optimize storage.

- Configured object transitions to **S3 Standard-IA** for less frequently accessed data.
- Configured expiration of **noncurrent object versions** to manage storage over time.

![Lifecycle Transition Rule](./screenshots/lifecycle1.png)

![Lifecycle Configuration](./screenshots/lifecycle11.png)

![Noncurrent Version Expiration](./screenshots/lifecycle2.png)

![S3 Lifecycle Rules](./screenshots/lifecycle3.png)

---

### 3. Implement a Disaster Recovery (DR) Strategy in Amazon S3

Enabled **S3 Versioning** and configured a separate **S3 bucket in another AWS Region** as a DR destination.

New objects uploaded to the source bucket are replicated to the destination bucket, providing a separate copy of the website data for **cross-region disaster recovery**.

![DR Bucket](./screenshots/drbucket.png)

![Cross-Region Replicated Objects](./screenshots/dr.png)

---

## 🔐 Data Protection

**S3 Versioning** was enabled on the source and DR buckets to protect against accidental overwrites and deletions.

A previous version of the website was also recovered and restored as the current object, demonstrating a practical **rollback and recovery** workflow.

![S3 Versioning](./screenshots/versioning1.png)

![Updated Website Version](./screenshots/newversion.png)

![Object Versions](./screenshots/versioning2.png)

---

## ☁️ AWS Skills Demonstrated

- Amazon S3
- Static Website Hosting
- S3 Versioning
- S3 Lifecycle Management
- S3 Standard-IA
- Cross-Region Replication (CRR)
- Data Protection
- Disaster Recovery
- Backup & Recovery
- Storage Optimization
