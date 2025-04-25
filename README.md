# Amazon-EC2-Backup-restore-using-AWS-Backup
# Overview

This lab demonstrates how to configure and use AWS Backup to create on-demand and automated backups of an EC2 instance, and how to restore a terminated EC2 instance using those backups.

---

## 🛠️ Part 1: Create EC2 Instance

- Launched an Ubuntu instance named `MyUbuntu-5756`.

![EC2 Instance List](screenshots_lab8/lab8_screenshot_1.png)

---

## 📦 On-Demand Backup with AWS Backup

- Enabled EC2 under Backup Settings.
- Created a new **Backup Vault** named `webapp-5756`.

![Backup Vault Settings](screenshots_lab8/lab8_screenshot_2.png)

- Created an **On-Demand Backup**.

![On-Demand Backup Settings](screenshots_lab8/lab8_screenshot_3.png)  
![Backup Jobs](screenshots_lab8/lab8_screenshot_4.png)

---

## 🔁 Automatic Backup via Backup Plan

- Created a Backup Plan: `mybackup-plan-5756`  
- Configured rule: `backup-rule-5756`

![Backup Plan Settings](screenshots_lab8/lab8_screenshot_5.png)

- Assigned EC2 instance to the backup plan using tag: `EC2/backup`

![Assign Resource to Plan](screenshots_lab8/lab8_screenshot_6.png)

- Verified backup plan details.

![Backup Plan Summary](screenshots_lab8/lab8_screenshot_7.png)

---

## ♻️ Restore EC2 Instance from Backup

- Terminated `MyUbuntu-5756` instance.
- Selected Recovery Point in Backup Vault.

![Recovery Point Details](screenshots_lab8/lab8_screenshot_8.png)

- Clicked Restore.

![Restore Job Created](screenshots_lab8/lab8_screenshot_9.png)

- Verified new EC2 instance after successful restore.

![Restored EC2 Instance](screenshots_lab8/lab8_screenshot_10.png)

---

## 🔍 Additional Screenshots

*(Optional extra visuals if needed for clarity)*

![Extra Screenshot 11](screenshots_lab8/lab8_screenshot_11.png)  
![Extra Screenshot 12](screenshots_lab8/lab8_screenshot_12.png)  
![Extra Screenshot 13](screenshots_lab8/lab8_screenshot_13.png)  
![Extra Screenshot 14](screenshots_lab8/lab8_screenshot_14.png)  
![Extra Screenshot 15](screenshots_lab8/lab8_screenshot_15.png)  
![Extra Screenshot 16](screenshots_lab8/lab8_screenshot_16.png)  
![Extra Screenshot 17](screenshots_lab8/lab8_screenshot_17.png)  
![Extra Screenshot 18](screenshots_lab8/lab8_screenshot_18.png)  
![Extra Screenshot 19](screenshots_lab8/lab8_screenshot_19.png)

---

## ✅ Summary

- Successfully configured both on-demand and scheduled EC2 backups.
- Verified restore capability by recreating a terminated instance using AWS Backup.
