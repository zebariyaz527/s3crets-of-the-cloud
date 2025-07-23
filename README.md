# s3crets-of-the-cloud
Beginner’s guide to launching an EC2 instance on AWS.
# 🚀 How to Launch Your First EC2 Instance on AWS – A Beginner’s Guide

Amazon EC2 (Elastic Compute Cloud) allows you to run virtual machines in the cloud. In this beginner-friendly guide, you’ll learn how to launch, connect, and manage your first EC2 instance — perfect for AWS Cloud Practitioner learners and future Cloud Support Engineers!

---

## ✅ Prerequisites

- An AWS account (Free Tier eligible)
- A web browser
- Basic familiarity with AWS Console (helpful but not required)

---

## 🛠 Step-by-Step: Launch Your EC2 Instance

### 1️⃣ Log in to the AWS Console
Go to [https://aws.amazon.com](https://aws.amazon.com) and sign in to the AWS Management Console.

---

### 2️⃣ Navigate to EC2
- Use the search bar to find and select **EC2**
- Click **Launch Instance**

---

### 3️⃣ Choose an Amazon Machine Image (AMI)
- Select: **Amazon Linux 2 AMI (HVM), SSD Volume Type**
- Eligible for free tier

---

### 4️⃣ Choose an Instance Type
- Select **t2.micro** (1 vCPU, 1 GB RAM)
- Free tier eligible

---

### 5️⃣ Configure Instance Details
- Leave default settings

---

### 6️⃣ Add Storage
- 8 GiB (default) is fine

---

### 7️⃣ Add Tags (Optional)
- Example: `Key: Name`, `Value: MyFirstEC2`

---

### 8️⃣ Configure Security Group
- Allow **SSH (port 22)** from **My IP**
- Important for secure access

---

### 9️⃣ Review and Launch
- Click **Launch**
- Create a new key pair → Download the `.pem` file
- Click **Launch Instances**

---

## 🔗 Connect to Your EC2 Instance

### Option 1: EC2 Instance Connect (Web Browser)
- Go to **Instances → Connect → EC2 Instance Connect**

### Option 2: SSH (Terminal)
```bash
ssh -i "my-key.pem" ec2-user@<your-public-ip>

chmod 400 my-key.pem


❗️ Don’t Forget to Stop or Terminate
To avoid unnecessary charges:

Go to EC2 Dashboard → Instances

Select your instance

Choose Instance State → Stop or Terminate


