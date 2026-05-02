# 🔐 Secure AWS EC2 Linux Web Server

## 📸 Final Result

![Final Server Verification](screenshots/23-final-server-verification.png)

> Deployed and secured a Linux-based web server on AWS EC2 using Apache, firewalld, and Fail2Ban.

---

## 💡 Project Overview

In this project, I built and secured a cloud-hosted Linux web server using AWS EC2. After deploying the server, I configured network access with security groups, installed Apache to host a webpage, and added additional security controls including a Linux firewall and Fail2Ban.

This project demonstrates both infrastructure deployment and basic system hardening.

---

## 🛠️ Technologies Used

- AWS EC2  
- Amazon Linux  
- Apache HTTP Server  
- SSH (Secure Shell)  
- Security Groups  
- firewalld (Linux firewall)  
- Fail2Ban (intrusion prevention)  
- Linux CLI  

---

## ⚙️ Deployment Walkthrough

### Step 1: EC2 Dashboard
![EC2 Dashboard](screenshots/01-ec2-dashboard.png)

---

### Step 2: Launch Instance
![Launch Instance](screenshots/02-launch-instance-name.png)

---

### Step 3: Select Amazon Linux
![Amazon Linux](screenshots/03-amazon-linux-selected.png)

---

### Step 4: Choose Instance Type
![Instance Type](screenshots/04-instance-type-selected.png)

---

### Step 5: Select Key Pair
![Key Pair](screenshots/05-key-pair-selected.png)

---

### Step 6: Configure Security Groups

Configured inbound rules:
- SSH (port 22)
- HTTP (port 80)
- HTTPS (port 443)

![Security Group](screenshots/06-security-group-rules.png)

---

### Step 7: Launch Success
![Launch Success](screenshots/07-instance-launch-success.png)

---

### Step 8: Instance Running
![Instance Running](screenshots/08-instance-running.png)

---

### Step 9: Public IP Address
![Public IP](screenshots/09-public-ip-address.png)

---

### Step 10: EC2 Connect
![EC2 Connect](screenshots/10-ec2-connect-page.png)

---

### Step 11: Terminal Access
![Terminal](screenshots/11-terminal-connected.png)

---

## 🐧 Linux Configuration

### Step 12: Update System

Command:
sudo yum update -y

![System Update](screenshots/12-system-update.png)

---

### Step 13: Install Apache

Command:
sudo yum install httpd -y

![Apache Installed](screenshots/13-apache-installed.png)

---

### Step 14: Start Apache

Commands:
sudo systemctl start httpd  
sudo systemctl enable httpd  

![Apache Started](screenshots/14-apache-started-enabled.png)

---

### Step 15: Verify Apache

Command:
sudo systemctl status httpd  

![Apache Status](screenshots/15-apache-status-running.png)

---

### Step 16: Test Web Server

Accessed via public IP in browser.

![Browser Test](screenshots/16-browser-apache-test-page.png)

---

## 🔐 Security Hardening

### Step 17: Install firewalld

Command:
sudo yum install firewalld -y  

![Firewalld Installed](screenshots/17-firewalld-installed.png)

---

### Step 18: Enable firewalld

Commands:
sudo systemctl start firewalld  
sudo systemctl enable firewalld  

![Firewalld Running](screenshots/18-firewalld-started-enabled.png)

---

### Step 19: Configure Firewall Rules

Commands:
sudo firewall-cmd --permanent --add-service=http  
sudo firewall-cmd --permanent --add-service=https  
sudo firewall-cmd --permanent --add-service=ssh  
sudo firewall-cmd --reload  

![Firewall Rules](screenshots/19-firewall-allowed-services.png)

---

### Step 20: Install Fail2Ban

Command:
sudo yum install fail2ban -y  

![Fail2Ban Installed](screenshots/20-fail2ban-installed.png)

---

### Step 21: Enable Fail2Ban

Commands:
sudo systemctl start fail2ban  
sudo systemctl enable fail2ban  

![Fail2Ban Running](screenshots/21-fail2ban-started-enabled.png)

---

### Step 22: Verify Fail2Ban

Command:
sudo systemctl status fail2ban  

![Fail2Ban Status](screenshots/22-fail2ban-status.png)

---

## ✅ Final Verification

### Step 23: Confirm Services Running

Verified:
- Apache running  
- firewalld active  
- Fail2Ban active  
- Website accessible  

![Final Verification](screenshots/23-final-server-verification.png)

---

## 🧠 What I Learned

- How to deploy cloud infrastructure using AWS EC2  
- How to configure secure remote access using SSH  
- How to install and manage Apache on Linux  
- How to configure a Linux firewall using firewalld  
- How Fail2Ban helps protect against unauthorized access attempts  
- How to validate a working and secured web server  

---

## 🔮 Future Improvements

- Add HTTPS using SSL/TLS  
- Configure domain name (Route 53)  
- Implement monitoring with CloudWatch  
- Automate deployment with Terraform  

---

## 📌 Author

Calvin Trammell  
https://github.com/calvin5731  
https://www.linkedin.com/in/calvin-trammell-56675295  
