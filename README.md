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

Configured an Amazon S3 bucket to host a static website containing HTML, CSS, and other static assets.

**Screenshot:**

![S3 Static Website Hosting](./screenshots/static-website-hosting.png)

---

### 2. Implement a data lifecycle strategy in Amazon S3

Configured an **S3 Lifecycle Rule** to automatically manage objects according to their lifecycle and optimize storage management.

**Screenshot:**

![S3 Lifecycle Configuration](./screenshots/lifecycle-rule.png)

---

### 3. Implement a disaster recovery (DR) strategy in Amazon S3

Enabled **S3 Versioning** to maintain previous versions of objects and provide a recovery mechanism in case of accidental deletion or overwriting.

**Screenshot:**

![S3 Versioning and Recovery](./screenshots/versioning-recovery.png)

---

## 📸 Project Screenshots

### Static Website

![Website](./screenshots/website.png)

### S3 Configuration

![S3 Configuration](./screenshots/s3-configuration.png)

### Lifecycle Management

![Lifecycle](./screenshots/lifecycle-rule.png)

### Disaster Recovery

![Versioning](./screenshots/versioning-recovery.png)
