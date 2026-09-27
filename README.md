# Cloud & Big Data (Hadoop) Quick Guide

When running a Big Data pipeline (like Hadoop or Spark) on the cloud (AWS), these six components handle your servers, storage, and security.

---

### 1. Compute & Networking

* **EC2 (Elastic Compute Cloud) — *Virtual Servers***
  * **What it is:** Rentable virtual computers in the cloud.
  * **In Hadoop:** Acts as your cluster nodes (NameNode and DataNodes) that process data.

* **VPC (Virtual Private Cloud) — *Private Network***
  * **What it is:** An isolated, private network inside the cloud.
  * **In Hadoop:** Keeps your EC2 Hadoop nodes hidden from the public internet while letting them share data privately at high speeds.

---

### 2. Storage & Permissions

* **S3 (Simple Storage Service) — *Cloud Storage***
  * **What it is:** Cheap, unlimited cloud storage that holds files in "buckets."
  * **In Hadoop:** Often replaces or backs up HDFS. You store massive datasets in S3 permanently and only turn on EC2 nodes when you need to process them.

* **IAM (Identity and Access Management) — *Access Control***
  * **What it is:** The permission system controlling *who* can access *what* in the cloud.
  * **In Hadoop:** Gives your EC2 nodes permission to read and write data in S3 buckets without hardcoding passwords.

---

### 3. Security & Encryption

* **SSL (Secure Sockets Layer) & TLS (Transport Layer Security) — *Data Encryption***
  * **What they are:** Protocols that encrypt data moving across a network (puts the `S` in `HTTPS`). **TLS** is simply the modern, secure upgrade to the older **SSL**.
  * **In Hadoop:** Encrypts sensitive data while it travels between S3 and your EC2 nodes, or between Hadoop nodes during a job.

---

### Quick Summary Table

| Term | Role | Hadoop Use Case |
| :--- | :--- | :--- |
| **EC2** | Virtual Server | Runs NameNode & DataNodes |
| **VPC** | Private Network | Isolates the Hadoop cluster |
| **S3** | Cloud Storage | Stores raw input & final output data |
| **IAM** | Permissions | Lets EC2 securely access S3 |
| **SSL / TLS** | Encryption | Protects data moving over the network |
