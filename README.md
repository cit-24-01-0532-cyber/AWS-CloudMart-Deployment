# AWS Scalable Web Infrastructure - Project CloudMart

This project showcases a professional deployment of a highly available and scalable web application on Amazon Web Services (AWS). It simulates a real-world scenario where a web store (CloudMart) is hosted with auto-healing and load-balancing capabilities.

## 🚀 Project Overview

The goal was to move beyond a single server setup and create an infrastructure that can handle traffic spikes and recover from server failures automatically.

### Key Features:
* **High Availability:** Instances are spread across multiple Availability Zones.
* **Auto-Scaling:** Automatically maintains a fleet of 2 EC2 instances.
* **Load Balancing:** Single DNS entry point to distribute traffic efficiently.
* **Security-First:** Custom Security Groups to control inbound and outbound traffic.

## 🛠️ Tech Stack & Services

* **Computing:** Amazon EC2 (Amazon Linux 2023)
* **Scaling:** AWS Auto Scaling Groups (ASG)
* **Traffic Management:** AWS Application Load Balancer (ALB)
* **Web Server:** Apache (HTTPD)
* **Network:** VPC, Public Subnets, Security Groups

## 🏗️ Architecture Details

1.  **Launch Template:** Defined the blueprint (AMI, Instance Type, Key Pair) and used **User Data** scripts to automate Apache installation.
2.  **Target Group:** Grouped EC2 instances and performed health checks on Port 80.
3.  **Application Load Balancer:** Configured as the internet-facing gateway to route traffic to healthy targets.
4.  **Auto Scaling Group:** Set with a `Desired Capacity` of 2, ensuring that if one instance fails, another is launched automatically.

## 📸 Deployment Success


The infrastructure was successfully tested using the Load Balancer DNS name, confirming that the traffic is being routed to the healthy EC2 fleet.

---
*Developed as part of my Cloud Computing learning journey.*
