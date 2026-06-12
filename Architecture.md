# Architecture Documentation

# Project Name

eSportArena Competitive Gaming Cloud

---

# Architecture Overview

The eSportArena Competitive Gaming Cloud project is designed and deployed on Amazon Web Services (AWS) to demonstrate practical cloud infrastructure implementation. The architecture focuses on providing a secure, scalable, and internet-accessible environment for hosting a gaming platform landing page while following cloud deployment best practices.

The infrastructure consists of networking components, compute resources, security configurations, and web hosting services that work together to provide a functional cloud environment.

---

# Architecture Diagram

The architecture diagram for this project is available in the diagrams folder.

Architecture Flow:

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

---

# AWS Infrastructure Components

## 1. Amazon Virtual Private Cloud (VPC)

A custom Virtual Private Cloud (VPC) was created to isolate project resources and provide a secure networking environment.

Configuration:

* VPC Name: eSportArena-VPC
* CIDR Block: 10.0.0.0/16

Purpose:

* Network isolation
* Secure communication
* Resource organization
* Infrastructure segmentation

Benefits:

* Enhanced security
* Controlled traffic management
* Scalable architecture
* Flexible network design

---

## 2. Public Subnet

A public subnet was configured inside the VPC.

Purpose:

* Host internet-facing resources
* Allow access from external users
* Support web application deployment

Resources Hosted:

* EC2 Instance
* Nginx Web Server
* Website Content

Benefits:

* Direct internet accessibility
* Easy deployment and management
* Supports web hosting services

---

## 3. Private Subnet

A private subnet was also created as part of the architecture.

Purpose:

* Future database deployment
* Internal application services
* Backend resource hosting

Benefits:

* Improved security
* Reduced external exposure
* Supports scalable architecture design

Although currently unused, the private subnet provides future expansion capability.

---

## 4. Internet Gateway

An Internet Gateway was attached to the VPC.

Purpose:

* Provide internet access to resources
* Enable inbound and outbound traffic
* Connect AWS resources with external users

Benefits:

* Public accessibility
* Web hosting support
* Internet connectivity

---

## 5. Security Group

A Security Group was configured to act as a virtual firewall for the EC2 instance.

Inbound Rules:

| Protocol | Port | Purpose               |
| -------- | ---- | --------------------- |
| SSH      | 22   | Secure Remote Access  |
| HTTP     | 80   | Website Access        |
| HTTPS    | 443  | Secure Website Access |

Purpose:

* Protect server resources
* Control incoming traffic
* Restrict unauthorized access

Benefits:

* Enhanced security
* Controlled communication
* Secure server administration

---

## 6. Amazon EC2 Instance

An Ubuntu-based Amazon EC2 instance was launched to host the website.

Configuration:

* Instance Type: t3.micro
* Operating System: Ubuntu Server 24.04 LTS

Purpose:

* Host web application
* Provide Linux environment
* Execute server-side operations

Benefits:

* Scalable computing
* Flexible deployment
* Cloud-based server management

---

## 7. Ubuntu Server

Ubuntu Server was selected as the operating system for the EC2 instance.

Purpose:

* Linux administration
* Web server hosting
* Application deployment

Activities Performed:

* System updates
* Package installation
* Nginx configuration
* Website deployment

Benefits:

* Stability
* Security
* Community support

---

## 8. Nginx Web Server

Nginx was installed and configured to host the eSportArena landing page.

Purpose:

* Serve web content
* Handle HTTP requests
* Manage website deployment

Benefits:

* High performance
* Low resource consumption
* Fast content delivery

Deployment Location:

/var/www/html/index.html

---

# Website Deployment Architecture

The website deployment process followed the sequence below:

1. Launch EC2 Instance
2. Connect using EC2 Instance Connect
3. Install Nginx
4. Configure Web Root Directory
5. Deploy Website Files
6. Restart Nginx Service
7. Verify Website Accessibility
8. Access Website via Public IP

---

# Security Architecture

The project follows basic cloud security practices:

* VPC Isolation
* Security Group Firewall Rules
* SSH-Based Administrative Access
* Controlled Network Exposure
* Public and Private Subnet Segmentation

Security Layers:

Internet User

↓

Security Group

↓

EC2 Instance

↓

Ubuntu Server

↓

Website

---

# Scalability Considerations

The architecture is designed for future expansion.

Possible Enhancements:

* Application Load Balancer
* Auto Scaling Groups
* Amazon RDS Database
* Amazon S3 Storage
* Amazon CloudWatch Monitoring
* Route 53 Domain Management
* SSL Certificate Integration
* Docker Containerization

---

# Cost Optimization Strategy

To minimize infrastructure cost:

* t3.micro EC2 Instance used
* Single instance deployment
* Minimal storage allocation
* Open-source Ubuntu Server
* Open-source Nginx Web Server

These choices ensure efficient resource utilization while maintaining functionality.

---

# Architecture Advantages

The implemented architecture provides:

* Secure Cloud Deployment
* Scalable Infrastructure
* Public Accessibility
* Linux-Based Hosting Environment
* Efficient Resource Management
* Practical AWS Implementation
* Future Expansion Capability

---

# Conclusion

The eSportArena Competitive Gaming Cloud architecture successfully demonstrates the implementation of core AWS services including VPC, Subnets, Security Groups, EC2, Ubuntu Server, and Nginx Web Server. The architecture provides a secure and scalable foundation for hosting web applications while showcasing essential cloud computing concepts and deployment practices.
