# High-Availability Web Architecture on AWS

## 📌 Project Overview
This project demonstrates a secure, scalable, and highly available 3-tier web architecture built in the **ap-south-1 (Mumbai)** region. The goal was to move beyond basic instance launching and build a production-ready environment using AWS best practices.

## 🏗️ Architecture

### Key Components:
* **Networking:** Custom VPC with 2 Public Subnets and 2 Private Subnets across multiple Availability Zones.
* **Compute:** EC2 instances managed by an **Auto Scaling Group (ASG)**.
* **Traffic Management:** **Application Load Balancer (ALB)** distributing traffic across instances.
* **Database:** **RDS MySQL** instance isolated in a private subnet.
* **Storage:** **Amazon S3** for persistent storage with **IAM Roles** for secure access.

## 🛠️ Skills Demonstrated
* **High Availability:** Configuring Multi-AZ subnets and Load Balancing.
* **Security:** Using Security Group nesting (Web-SG -> DB-SG) and private subnets.
* **Automation:** Bootstrapping EC2 instances using **User Data** scripts.
* **Identity Management:** Implementing IAM Roles for service-to-service communication.

## 🚀 Troubleshooting
During the build, I successfully resolved:
* **502 Bad Gateway:** Identified missing Public IPs on EC2 instances within a custom VPC.
* **SSH Connectivity:** Debugged Security Group rules to allow restricted access via "My IP."  
