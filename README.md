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
![LAMP 3](https://github.com/user-attachments/assets/9164c3f2-1f2b-4fd3-b53f-7f8889b7210f)


## ⚙️ Step 1: Update the Package Manager

After connecting to your EC2 instance, it is recommended to update the package manager to ensure that all packages are up to date.

![Lamp 4](https://github.com/user-attachments/assets/422db418-b812-47c1-8cf5-8381054fb620)




## 🌐 Step 2: Install Apache2

Apache is a widely used open-source web server software that will serve your web pages to users over the internet.

![LAMP 5](https://github.com/user-attachments/assets/951bd47f-6cd8-4aa8-8ec6-b7192efd4ac5)


### ⚙️ Enable and Check Apache Service

To ensure Apache starts automatically on system boot and to verify that it is running properly, use the following commands:

#### 🖥️ Commands:

```bash
sudo systemctl enable apache2
sudo systemctl status apache2

![LAMP 6](https://github.com/user-attachments/assets/50aa93f5-9fea-4756-a68d-95b0aab251e6)

🌍 Step 5: Test Apache Externally (From Browser)
To confirm that Apache is accessible over the internet, open your browser and visit the public IP of your EC2 instance:

cpp
Copy
Edit
http://<your-ec2-public-ip>:80
🔍 Example:
cpp
Copy
Edit
http://13.53.216.202:80
You should see the Apache2 Ubuntu Default Page, indicating that your server is successfully serving web pages.



