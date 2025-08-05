# 📘 LAMP Stack Implementation on AWS (EC2)
> **Linux | Apache | MySQL | PHP**

---

## 🧭 Introduction
The **LAMP stack** is a popular open-source web development platform used for hosting dynamic websites and web applications. It consists of four main components:

- **L**inux: The operating system  
- **A**pache: The web server  
- **M**ySQL: The relational database management system  
- **P**HP: The programming language (can also be replaced with Python or Perl)

This guide provides step-by-step instructions on how to set up and configure a LAMP stack on an **AWS EC2 instance** running **Ubuntu 24.04 LTS**.

---

## 🔧 Step 0: Preparing the Environment

Before we install the LAMP stack, we need to launch and prepare an EC2 instance.

### ✅ Tasks:

1. **Launch EC2 Instance:**
   - Log in to your AWS Management Console.
   - Navigate to **EC2 > Instances > Launch Instance**.
   - Choose an **Ubuntu 24.04 LTS AMI**.
   - Select the **t2.micro** instance type (Free Tier eligible).
   - Choose a region closest to your location (e.g., `eu-west-2a`).
   - Create a new key pair or use an existing one to SSH into the server.
   - Open necessary ports (SSH - 22, HTTP - 80) in the **Security Group**.
  
   - ![LAMP](https://github.com/user-attachments/assets/430b72e9-2916-45a6-83b9-8b6ea3c3b21f)
   - ![LAMP 2](https://github.com/user-attachments/assets/77081c4d-d413-4d35-8053-e17143822269)



2. **Connect to the Instance:**
   Use the `.pem` file and connect via SSH:

   ```bash
   ssh -i "your-key-name.pem" ubuntu@<your-ec2-public-ip>
Replace your-key-name.pem with your actual key file and <your-ec2-public-ip> with the public IP of your instance.
