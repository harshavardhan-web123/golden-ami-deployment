# 🖼️ Golden AMI Deployment on AWS

## 📌 Project Overview
This project demonstrates how to create and use a **Golden AMI (Amazon Machine Image)** to deploy multiple identical EC2 instances with the same configuration.

The goal is to ensure consistency, faster deployment, and scalability by reusing a pre-configured server image.

---

## 🎯 Objective
- Configure a base EC2 instance with a web server
- Create a Golden AMI from the configured instance
- Launch multiple EC2 instances using the AMI
- Verify identical configuration across all instances

---

## 🛠️ Technologies & Services Used
- AWS EC2 (Elastic Compute Cloud)
- Amazon AMI (Golden AMI)
- Amazon S3 (Private Bucket - optional)
- Apache Web Server (httpd)
- Linux

---
## 🏗️ Architecture Diagram
Configured EC2 → Create AMI → Launch Multiple EC2 → Same Web Application


---

## 🔄 Workflow

1. Launch an EC2 instance
2. Install Apache web server (httpd)
3. Deploy a sample web application (index.html)
4. Create a Golden AMI from the configured instance
5. Launch multiple EC2 instances using the AMI
6. Start web server on each instance
7. Verify application output using public IP

---

## ⚙️ Setup Steps

### 🔹 Step 1: Launch EC2 Instance
- Create an EC2 instance
- Connect using SSH

---

### 🔹 Step 2: Install Apache

sudo yum install httpd -y
sudo systemctl start httpd

Step 3: Deploy Web Application
cd /var/www/html
sudo vi index.html

Add sample content:

This is my project website

Step 4: Create Golden AMI
Go to EC2 Dashboard
Select instance → Actions → Create Image
Name: golden-ami-webserver
🔹 Step 5: Launch Instances from AMI
Use created AMI
Launch multiple EC2 instances (e.g., Webserver1, Webserver2)
🔹 Step 6: Start Web Server
sudo systemctl start httpd
🔹 Step 7: Verify Output
Access each instance using public IP
Confirm same application is running
📸 Screenshots

(Add your screenshots here)

EC2 Instance Setup
Apache Installation
Application Output
AMI Creation
Multiple EC2 Instances
Final Output from Webserver1 & Webserver2
✅ Key Features
Consistent server configuration
Faster deployment using AMI
Scalable infrastructure
Reusable machine image
📈 Benefits
Reduces manual configuration
Saves time in deployment
Ensures uniform environment
Easy scaling of servers
🚀 Future Enhancements
Integrate with Auto Scaling
Use Load Balancer for traffic distribution
Automate AMI creation using scripts
Add monitoring using CloudWatch

👨‍💻 Author

Harshavardhan
BCA Student | Aspiring Cloud & DevOps Engineer

