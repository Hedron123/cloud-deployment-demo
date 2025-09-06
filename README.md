# cloud-deployment-demo
# 🌐 Cloud Deployment of a Simple Web Application on AWS EC2

## 👨‍🎓 Project Details
- **Student Name:** Aditya Maheshwari  
- **Registration Number:** 229301363  
- **Course/Subject:** Cloud Computing / IaaS Deployment  
- **Project Type:** Basic Web Application Deployment with Security Hardening  

---

## 📌 Project Overview
This project demonstrates the deployment of a **simple static web application** on an **AWS EC2 instance** using **Amazon Linux AMI** and **Nginx** as the web server.  

The application is a styled **HTML frontend page** that includes the student’s name and registration number.  
The project also covers basic **infrastructure setup, deployment, and security hardening steps** to improve the server’s security posture.  

---

## 🛠️ Technologies Used
- **Cloud Provider:** Amazon Web Services (AWS)  
- **Service Used:** Elastic Compute Cloud (EC2) – Infrastructure as a Service (IaaS)  
- **Operating System:** Amazon Linux 2 AMI  
- **Web Server:** Nginx  
- **Frontend:** HTML, CSS  

---

## 🚀 Step-by-Step Deployment Guide

### 1️⃣ Launch an EC2 Instance
1. Log in to the **AWS Management Console**.  
2. Navigate to **EC2** → **Launch Instance**.  
3. Configure:
   - **AMI:** Amazon Linux 2 (Free Tier Eligible).  
   - **Instance Type:** t2.micro (Free Tier).  
   - **Key Pair:** Create/Use existing `.pem` file for SSH.  
   - **Security Group:** Allow ports `22 (SSH)` and `80 (HTTP)`.  
   - **Storage:** Default 8 GB.  
4. Launch the instance.  

---

### 2️⃣ Connect to EC2 Instance
Use SSH from your local terminal:
   bash
ssh -i my-key.pem ec2-user@<your-public-ip>

---

### 3️⃣ Install and Start Nginx
Run the following commands:

bash
Copy code
sudo yum update -y
sudo amazon-linux-extras enable nginx1
sudo yum install nginx -y
sudo systemctl start nginx
sudo systemctl enable nginx
Verify Nginx is running:

bash
Copy code
systemctl status nginx

---

### 4️⃣ Deploy the HTML Web Page
Go to the default Nginx directory:

bash
Copy code
cd /usr/share/nginx/html/
Replace the default index.html with your custom webpage:

bash
Copy code
sudo nano index.html
Paste your HTML code (with colors, name, and registration number).

Save and exit.

---

### 5️⃣ Access the Web Application
Open your browser.

Enter your Public IP → http://<your-ec2-ip>

You should see your custom page 🎉

<img width="2880" height="1476" alt="Screenshot 2025-09-05 145236" src="https://github.com/user-attachments/assets/38d9dcea-6e1b-4681-8978-6de6d5e15da3" />

<img width="2880" height="1478" alt="Screenshot 2025-09-05 145124" src="https://github.com/user-attachments/assets/0820801a-3d4d-4217-b3bf-1bd43980bad8" />

<img width="2880" height="1476" alt="Screenshot 2025-09-05 145053" src="https://github.com/user-attachments/assets/17a2fdf1-46b0-44d5-8d55-004e971e9c03" />

<img width="2880" height="1480" alt="Screenshot 2025-09-05 145027" src="https://github.com/user-attachments/assets/629d1eaf-3f5f-4e80-8fe1-cc43f5cfeb63" />
