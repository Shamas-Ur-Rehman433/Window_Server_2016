# Window_Server_2016
# Windows Server 2016 – Active Directory Domain Services (AD DS) Lab

## Overview

This project demonstrates the deployment and configuration of a Windows Server 2016 Active Directory environment in a virtual lab. The purpose of this lab is to build a strong foundation in Windows Server administration by performing real-world system administration tasks commonly used in enterprise environments.

The project documents every major configuration step with screenshots, making it easy for recruiters, hiring managers, and fellow learners to understand the implementation process.

---

# Objectives

- Configure a static IPv4 address
- Rename the server
- Verify network connectivity
- Install Active Directory Domain Services (AD DS)
- Promote the server to a Domain Controller
- Create a new Active Directory forest and domain
- Create Organizational Units (OUs)
- Create Active Directory users
- Create Security Groups
- Join a Windows client computer to the domain
- Verify the Active Directory environment

---

# Lab Environment

| Component | Details |
|-----------|---------|
| Operating System | Windows Server 2016 |
| Client Operating System | Windows 10 / Windows 11 |
| Virtualization Platform | VMware Workstation |
| Server Name | DC01 |
| Domain Name | gift.local |
| Network Type | Private Lab Network |

---

# Network Configuration

| Setting | Value |
|---------|-------|
| IP Address | 192.168.210.10 |
| Subnet Mask | 255.255.255.0 |
| Default Gateway | 192.168.210.2 |
| Preferred DNS | 192.168.210.10 |

---

# Project Tasks

---

## 2. Static IP Configuration

### Tasks Performed

- Configured IPv4 settings
- Assigned Static IP
- Configured Gateway
- Configured DNS Server

### Screenshots/01-Network

- Network Adapter Properties
- IPv4 Configuration
- ipconfig /all Output

---

## 3. Server Configuration

### Tasks Performed

- Renamed the server to **DC01**
- Restarted the server
- Verified the computer name

### Screenshots/00_Server Configuration

- System Properties
- Computer Name

---

## 4. Network Connectivity Test

### Tasks Performed

- Verified local network connectivity
- Verified internet connectivity
- Verified DNS resolution

### Commands Used

```cmd
ping 8.8.8.8

ping google.com

ipconfig /all
```

### Screenshots/01-Network

- Ping Results
- IP Configuration

---

## 5. Active Directory Domain Services Installation

### Tasks Performed

- Opened Server Manager
- Added Roles and Features
- Installed Active Directory Domain Services

### Screenshots/02-ADDS

- Server Roles
- AD DS Installation
- Installation Successful

---

## 6. Domain Controller Promotion

### Tasks Performed

- Promoted the server to Domain Controller
- Created a new forest
- Created a new domain
- Configured Directory Services Restore Mode (DSRM)
- Completed prerequisite checks

### Domain

```
gift.local
```

### Screenshots/03-Domain-Controller

- Deployment Configuration
- Domain Configuration
- Installation Complete

---

## 7. Active Directory Verification

### Tasks Performed

- Logged in as Domain Administrator
- Verified Active Directory installation
- Opened Active Directory Users and Computers

### Screenshots/03-Domain-Controller

- Domain Login
- ADUC Console

---

## 8. Organizational Units (OUs)

### Organizational Structure

```
Company
│
├── IT
├── HR
├── Finance
├── Accounts
├── Sales
├── Management
└── Support
```

### Tasks Performed

- Created Organizational Units
- Verified OU hierarchy

### Screenshots/04-OU

- OU Structure

---

## 9. User Management

### Tasks Performed

Created multiple Active Directory users including:

- Ahmed
- Akbar
- Ali
- Asia

### Screenshots/05-Users

- User List
- User Properties

---

## 10. Security Groups

### Groups Created

- IT_Admins
- HR_Group
- Finance_Group

### Screenshots/06-Groups

- Security Groups
- Group Properties

---

## 11. Domain Join

### Tasks Performed

- Configured Windows client
- Joined client to the domain
- Restarted the client
- Logged in using a domain account

### Screenshots/07-Client-Join

- Client System Properties
- Domain Join
- Domain Login

---

# Project Structure

```
Windows-Server-2016-ADDS

│
├── README.md
│
├── Documentation
│
├── Screenshots
│   ├── 02_Static_IP.png
│   ├── 03_IPConfig_All.png
│   ├── 04_Server_Name.png
│   ├── 05_Ping_Test.png
│   ├── 06_ADDS_Role.png
│   ├── 07_Install_Success.png
│   ├── 08_Promote_DC.png
│   ├── 09_Domain_Created.png
│   ├── 10_ADUC.png
│   ├── 11_OUs.png
│   ├── 12_Users.png
│   ├── 13_Groups.png
│   └── 14_Client_Domain_Join.png
│
```

---

# Skills Demonstrated

- Windows Server 2016 Administration
- Active Directory Domain Services
- Domain Controller Deployment
- Static IP Configuration
- DNS Configuration
- Active Directory Users and Computers
- Organizational Unit Management
- User and Group Administration
- Windows Client Domain Join
- Basic Network Troubleshooting

---

# Learning Outcomes

After completing this project, I gained practical experience in:

- Installing and configuring Windows Server 2016
- Managing Active Directory infrastructure
- Deploying a Domain Controller
- Creating and organizing Active Directory objects
- Configuring networking for Windows Server
- Managing users and security groups
- Joining client computers to an Active Directory domain
- Documenting enterprise IT configurations for professional portfolios

---

# Author

**Shamsur Rehman**

BS Computer Science

Aspiring System Administrator | Network Engineer | Cloud Engineer

