AWS 3-Tier Application Deployment Project
📌 Project Overview

This project demonstrates the deployment of a 3-Tier Web Application Architecture on AWS using best practices for scalability, security, and high availability.

The architecture separates the application into three layers:

Presentation Layer (Web Tier)

Application Layer (App Tier)

Database Layer (DB Tier)

This project simulates a real-world production environment where the web servers handle user requests, the application servers process business logic, and the database securely stores data.

🏗 Architecture Diagram

(You can add your architecture diagram image here)

User
  │
  ▼
Internet
  │
  ▼
Web Server (Nginx)
  │
  ▼
Internal Load Balancer
  │
  ▼
Application Servers
  │
  ▼
RDS MySQL Database
☁ AWS Services Used

Amazon VPC – Custom network environment

EC2 – Web and Application servers

Application Load Balancer – Distribute traffic between servers

Amazon RDS (MySQL) – Managed relational database

Amazon S3 – Private bucket for storing application code

IAM Role – Secure access between services

Security Groups – Network level security

VPC Endpoints / SSM – Secure connectivity without public access

📂 Project Architecture
1️⃣ Network Layer

Created custom VPC: 192.168.0.0/16

Public and Private Subnets

Internet Gateway & Route Tables

2️⃣ Security Layer

Configured 5 Security Groups

Restricted communication between tiers

3️⃣ Storage Layer

Created Private S3 Bucket

Stores application source code

4️⃣ Database Layer

Deployed Amazon RDS MySQL

Database hosted in private subnet

5️⃣ Application Layer

Created EC2 App Servers

Installed required dependencies

Connected to RDS Database

6️⃣ Load Balancing

Configured Internal Load Balancer

Routes traffic to App Servers

7️⃣ Web Layer

Created Web Server EC2 Instance

Installed and configured Nginx

Nginx forwards requests to internal load balancer

⚙ Deployment Steps

Create Custom VPC (192.168.0.0/16)

Configure Subnets and Route Tables

Create Security Groups

Create Private S3 Bucket to store application code

Create IAM Role with SSM permissions

Deploy Amazon RDS MySQL

Launch Application Servers (EC2) and configure application

Configure Internal Load Balancer

Launch Web Server (EC2) and configure Nginx

Test the application end-to-end

🔐 Security Best Practices Implemented

Private subnets for App and Database layers

Restricted Security Group rules

IAM roles instead of access keys

Private S3 bucket

Internal Load Balancer for app layer isolation

📊 Key Learning Outcomes

Designing 3-Tier Architecture in AWS

VPC networking and subnet design

Security groups and IAM roles

Application deployment on EC2

Database integration with RDS

Load balancing and request routing

Secure architecture implementation

🚀 Future Improvements

Auto Scaling for Web and App servers

CI/CD pipeline using GitHub Actions / Jenkins

Infrastructure as Code using Terraform

Monitoring using CloudWatch

👨‍💻 Author

Faisal
Cloud / DevOps Enthusiast

GitHub:
https://github.com/awsfaisal
