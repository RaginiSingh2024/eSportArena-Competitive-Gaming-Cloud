# 🎮 eSportArena Competitive Gaming Cloud

## Project Overview

eSportArena Competitive Gaming Cloud is a cloud infrastructure project developed on Amazon Web Services (AWS) to demonstrate enterprise-level cloud deployment, networking, security, Linux administration, and web hosting concepts.

The project was designed as part of the AWS Case Study Problem Statement provided by ITM Skills University. The primary objective is to create a scalable, secure, and cloud-hosted gaming platform environment capable of supporting future expansion requirements while demonstrating practical cloud computing concepts.

The solution utilizes AWS networking services, virtual servers, Linux administration, and web hosting technologies to deploy and manage a gaming platform landing page on the cloud.

---
## 🏗️ AWS Architecture Diagram

![AWS Architecture](diagrams-architecture/AWS_Architecture.drawio.png)


## 📸 Deployment Screenshots

### AWS Login
![AWS Login](screenshots/aws_login_page.png)

### VPC Created
![VPC Created](screenshots/SS-02-VPC-Created.png)

### VPC List
![VPC List](screenshots/SS-02-VPC-List.png)

### Resource Map
![Resource Map](screenshots/SS-03-Resource-Map.png)

### Subnets
![Subnets](screenshots/SS-03-Subnets.png)

### EC2 Configuration
![EC2 Configuration](screenshots/SS-04-EC2-Configuration.png)

### Key Pair Created
![Key Pair](screenshots/SS-05-KeyPair-Created.png)

### Security Group Rules
![Security Group](screenshots/SS-07-Security-Group-Rules.png)

### EC2 Launch Configuration
![EC2 Launch](screenshots/SS-08-EC2-Launch-Configuration.png)

### EC2 Running Instance
![EC2 Running](screenshots/SS-09-EC2-Running-Instance.png)

### EC2 Started Again
![EC2 Restart](screenshots/SS-09-EC2-Started-Again.png)

### EC2 Terminal Connected
![EC2 Terminal](screenshots/SS-10-EC2-Terminal-Connected.png)

### MySQL Running
![MySQL](screenshots/SS-10-MySQL-Running.png)

### Linux User Created
![Linux User](screenshots/SS-11-Linux-User-Created.png)

### Nginx Service Running
![Nginx](screenshots/SS-11-Nginx-Service-Running.png)

### Permissions
![Permissions](screenshots/SS-12-Permissions.png)

### Cron Job
![Cron Job](screenshots/SS-13-CronJob.png)

### Docker Installed
![Docker Installed](screenshots/SS-14-Docker-Installed.png)

### Docker Container
![Docker Container](screenshots/SS-15-Docker-Container.png)

### Shell Script
![Shell Script](screenshots/SS-16-Shell-Script.png)

### IAM User
![IAM User](screenshots/SS-17-IAM-User.png)

### S3 Bucket
![S3 Bucket](screenshots/SS-18-S3-Bucket.png)

### CloudWatch Metrics
![CloudWatch](screenshots/SS-19-CloudWatch-Metrics.png)

### Website Home Page
![Website Home](screenshots/Website Home Page.png)

### Website Features Section
![Website Features](screenshots/Website Features Section.png)

### Website Architecture Section
![Website Architecture](screenshots/Website Architecture Section.png)

## Technologies Used

- AWS EC2
- AWS VPC
- Security Groups
- Ubuntu 24.04
- Nginx
- HTML
- Draw.io

# Problem Statement

The eSportArena Competitive Gaming Cloud platform requires a centralized cloud environment capable of supporting operational management, scalability, monitoring, reporting, and secure access control.

The existing environment relies on disconnected systems and manual workflows. Therefore, a modern cloud-based architecture was designed using AWS services to improve:

* Scalability
* Availability
* Security
* Cloud Deployment
* Infrastructure Management
* Performance Monitoring
* Future Expansion Capabilities

---

# Project Objectives

The primary objectives of this project are:

* Design a cloud infrastructure using AWS.
* Create an isolated network using Amazon VPC.
* Configure public and private subnets.
* Deploy a Linux-based EC2 virtual machine.
* Configure secure network access using Security Groups.
* Install and manage a web server using Nginx.
* Deploy a responsive gaming platform landing page.
* Demonstrate Linux Administration concepts.
* Implement cloud deployment best practices.
* Showcase practical cloud computing implementation.

---
## Architecture

See Architecture.md and diagrams folder.

# AWS Services Used

| Service          | Purpose                   |
| ---------------- | ------------------------- |
| Amazon EC2       | Virtual Server Hosting    |
| Amazon VPC       | Network Isolation         |
| Public Subnet    | Internet Facing Resources |
| Private Subnet   | Internal Resources        |
| Security Groups  | Firewall Configuration    |
| Ubuntu Server    | Operating System          |
| Nginx            | Web Server                |
| Internet Gateway | Internet Connectivity     |

---

# Solution Architecture

The project architecture follows a secure AWS deployment model.

Internet User

↓

Internet Gateway

↓

Security Group

↓

Public Subnet

↓

EC2 Instance

↓

Ubuntu Server

↓

Nginx Web Server

↓

eSportArena Website

The infrastructure is deployed inside a custom VPC and follows AWS networking best practices.

---

## 📂 Project Structure
```text
eSportArena-Competitive-Gaming-Cloud
│
├── README.md
├── Architecture.md
├── AWS_Final_Documentation_Ragini_023.pdf
│
├── deployment
│   └── deployment_steps.md
│
├── diagrams-architecture
│   └── AWS_Architecture.drawio.png
│
├── screenshots
│   ├── 01_vpc_created.png
│   ├── 02_subnets.png
│   ├── 03_security_group.png
│   ├── 04_ec2_running.png
│   ├── 05_nginx_running.png
│   ├── 06_website_homepage.png
│   ├── 07_features_section.png
│   └── 08_architecture_section.png
│
└── website
    └── index.html
```

# Infrastructure Components

## 1. Virtual Private Cloud (VPC)

A custom VPC was created to provide network isolation and secure communication between resources.

Configuration:

* VPC Name: eSportArena-VPC
* CIDR Block: 10.0.0.0/16

---

## 2. Public Subnet

The public subnet hosts internet-facing resources such as the EC2 instance.

Purpose:

* Website Hosting
* Internet Access
* Public Connectivity

---

## 3. Private Subnet

A private subnet was created for future backend services and database deployment.

Purpose:

* Secure Resource Deployment
* Database Hosting
* Internal Communication

---

## 4. Security Group

A Security Group was configured as a virtual firewall.

Allowed Ports:

* SSH (22)
* HTTP (80)
* HTTPS (443)

This ensures secure administrative access while allowing web traffic.

---

## 5. EC2 Instance

An Ubuntu-based EC2 virtual machine was launched and configured.

Configuration:

* Instance Type: t3.micro
* Operating System: Ubuntu Server 24.04 LTS

Purpose:

* Application Hosting
* Linux Administration
* Web Service Deployment

---

## 6. Nginx Web Server

Nginx was installed and configured on the EC2 instance.

Purpose:

* Host Website
* Handle Client Requests
* Serve Static Content

---

# Linux Administration Tasks Performed

The following Linux administration tasks were performed:

* Package Updates
* Web Server Installation
* Service Management
* File Management
* Nginx Configuration
* Website Deployment

Commands Used:

```bash
sudo apt update
sudo apt install nginx -y
sudo systemctl start nginx
sudo systemctl enable nginx
sudo systemctl restart nginx
sudo systemctl status nginx
```

---

# Website Deployment

A custom gaming-themed landing page was developed and deployed using Nginx.

Features:

* Responsive Design
* Gaming Theme Interface
* AWS Cloud Branding
* Architecture Visualization
* Project Statistics Section
* Cloud Deployment Showcase

The website was successfully hosted on the EC2 instance and accessed through the public IP address.

---

# Implementation Workflow

Step 1: Create VPC

Step 2: Configure Public and Private Subnets

Step 3: Configure Security Group Rules

Step 4: Launch Ubuntu EC2 Instance

Step 5: Connect to EC2

Step 6: Install Nginx

Step 7: Deploy Website Files

Step 8: Restart Web Server

Step 9: Verify Website Access

Step 10: Document Infrastructure

---

# Project Screenshots

The following implementation screenshots are included in the project documentation:

* VPC Creation
* Subnet Configuration
* Security Group Setup
* EC2 Deployment
* Ubuntu Server Access
* Nginx Installation
* Website Hosting
* Architecture Diagram

---

# Key Learning Outcomes

This project provided hands-on experience with:

* Cloud Infrastructure Deployment
* AWS Networking
* Virtual Machine Management
* Linux Administration
* Web Hosting
* Security Configuration
* Cloud Architecture Design
* Infrastructure Documentation

---

# Future Enhancements

The project can be enhanced by implementing:

* AWS Load Balancer
* Auto Scaling
* Amazon RDS
* Amazon S3 Storage
* CloudWatch Monitoring
* Route 53 Domain Integration
* SSL Certificates
* Docker Containerization
* Multi-Region Deployment

---

# Conclusion

The eSportArena Competitive Gaming Cloud project successfully demonstrates the deployment of a secure and scalable cloud infrastructure using AWS services. The project highlights practical implementation of networking, server administration, web hosting, and cloud deployment concepts while providing a strong foundation for future enterprise-scale cloud solutions.

---

# Developed By

Ragini Singh

B.Tech Computer Science and Engineering

Problem Statement No : 90

PS Title : eSportArena Competitive Gaming Cloud

ITM Skills University

AWS Case Study Project
