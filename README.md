# 🖥️ AWS EC2 Web Server Project

This project demonstrates how to deploy a simple web server on an **Amazon EC2 instance** using **Amazon Linux 2023** and the **Apache (httpd)** web server.
The EC2 instance hosts a basic HTML webpage located in `/var/www/html/index.html`.

---

## 🚀 Project Overview

This project shows the full process of:

* Launching an EC2 instance
* Connecting through SSH
* Installing and configuring Apache
* Hosting a custom HTML webpage
* Managing security groups
* Documenting the project using Git & GitHub

---

## 🔧 Steps Performed

### 1️⃣ Launch EC2 Instance

* Instance type: **t3.micro** (Free Tier eligible)
* OS: **Amazon Linux 2023**
* Storage: 8GB gp3
* Security group:

  * **Port 22 (SSH)** — My IP only
  * **Port 80 (HTTP)** — Allow from anywhere

---

### 2️⃣ Connect via SSH

```bash
ssh -i fausto-key.pem ec2-user@http://18.133.245.177/
```

---

### 3️⃣ Install Apache (httpd)

```bash
sudo yum update -y
sudo yum install -y httpd
sudo systemctl start httpd
sudo systemctl enable httpd
```

---

### 4️⃣ Create Website Content

Created the file:

**/var/www/html/index.html**

```html
<h1>Welcome to Fausto's EC2 Web Server</h1>
<p>This website is served from Apache running on Amazon EC2.</p>
```

---

### 5️⃣ Verify the Website

Opened the browser and visited:

```
http://http://18.133.245.177/
```

The custom webpage loaded successfully.

---

## 📁 Project Files

| File         | Description                |
| ------------ | -------------------------- |
| `README.md`  | Project documentation      |
| `index.html` | HTML webpage hosted on EC2 |

---

## 🧠 Skills Demonstrated

* AWS EC2 provisioning
* Security Groups configuration
* Linux CLI (Amazon Linux)
* Apache Web Server administration
* SSH key-based authentication
* Git & GitHub version control
* Cloud project documentation

---

## 📸 Screenshot Example (optional)

You can add a screenshot of your EC2 website like this:
<img width="578" height="208" alt="Screenshot 2025-11-13 at 21 02 21" src="https://github.com/user-attachments/assets/3a2b0328-6673-4d51-8547-81ab0a583ad3" />

```
![EC2 Web Server Screenshot](screenshot.png)
```<img width="642" height="881" alt="Screenshot 2025-11-13 at 21 14 50" src="https://github.com/user-attachments/assets/e0e7c569-501c-4ba1-98a9-4b6a0918b99a" />


---

## 👤 Author

**Fausto Sacco**
Cloud Computing Engineer in Training
AWS re/Start Student

