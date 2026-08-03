# Window_Server_2016
# Domain Controller Configuration

## Overview

This document explains how the Windows Server 2016 machine was promoted to a **Domain Controller (DC)** by installing **Active Directory Domain Services (AD DS)** and creating a new Active Directory forest.

A Domain Controller is a Windows Server that stores the Active Directory database, authenticates users and computers, applies Group Policies, and provides centralized management for an organization's network.

---

# Objectives

- Install Active Directory Domain Services (AD DS)
- Promote the server to a Domain Controller
- Create a new Active Directory forest
- Create a new domain
- Configure Directory Services Restore Mode (DSRM)
- Verify successful Domain Controller installation

---

# Prerequisites

Before promoting the server to a Domain Controller, ensure the following:

- Windows Server 2016 is installed.
- A static IPv4 address is configured.
- The server has been renamed to **DC01**.
- Network connectivity is verified.
- The server has administrative privileges.

---

# Environment

| Component | Value |
|-----------|-------|
| Operating System | Windows Server 2016 |
| Server Name | DC01 |
| Server Role | Domain Controller |
| Domain Name | company.local |
| Forest Functional Level | Windows Server 2016 |
| Domain Functional Level | Windows Server 2016 |

---

# Server Information

| Setting | Value |
|---------|-------|
| Computer Name | DC01 |
| IP Address | 192.168.210.10 |
| DNS Server | 192.168.210.10 |
| Domain | gift.local |

---

# Procedure

## Step 1

Open **Server Manager**.

---

## Step 2

Select:

```
Manage

↓

Add Roles and Features
```

---

## Step 3

Choose:

```
Role-based or feature-based installation
```

Click **Next**.

---

## Step 4

Select the local server.

Click **Next**.

---

## Step 5

Select:

```
Active Directory Domain Services (AD DS)
```

Click **Add Features**.

Click **Next** until the installation page appears.

---

## Step 6

Click:

```
Install
```

Wait until the installation is completed.

---

## Step 7

After the installation is complete, click:

```
Promote this server to a domain controller
```

---

## Step 8

Choose:

```
Add a new forest
```

Enter the root domain name:

```
gift.local
```

Click **Next**.

---

## Step 9

Configure the following:

- Forest Functional Level
- Domain Functional Level
- DNS Server
- Global Catalog (GC)

Enter the **Directory Services Restore Mode (DSRM)** password.

> 

Click **Next**.

---

## Step 10

Review the DNS Options.

Click **Next**.

---

## Step 11

Verify the NetBIOS domain name.

Example:

```
gift
```

Click **Next**.

---

## Step 12

Review the database, log files, and SYSVOL paths.

Use the default locations unless a custom configuration is required.

Click **Next**.

---

## Step 13

Review all configuration settings.

Click **Next**.

---

## Step 14

Wait for the **Prerequisites Check** to complete.

If all checks pass successfully, click:

```
Install
```

The server will automatically restart after the installation.

---

## Step 15

After the restart, log in using the domain administrator account.

Example:

```
gift\Administrator
```

---

# Verification

Verify the following:

- The server is functioning as a Domain Controller.
- Active Directory Users and Computers opens successfully.
- The domain **gift.local** exists.
- The Domain Controller appears healthy in Server Manager.



# Screenshots

Store screenshots in:

```
Screenshots/03-Domain-Controller/
```

Recommended screenshots:

- Server Manager
- Add Roles and Features Wizard
- Active Directory Domain Services Selected
- Deployment Configuration
- Installation Complete
- Domain Login Screen
- Active Directory Users and Computers
- Server Manager Dashboard

---

# Result

Successfully promoted the Windows Server 2016 machine to a **Domain Controller** by installing **Active Directory Domain Services (AD DS)** and creating the **company.local** domain.

The server now provides centralized authentication, directory services, DNS integration, and Active Directory management for all domain-joined computers and users.

---

# Benefits of a Domain Controller

- Centralized authentication
- Centralized user management
- Group Policy deployment
- DNS integration
- Secure access control
- Simplified administration
- Enterprise scalability
- Improved network security

---

# Skills Demonstrated

- Windows Server 2016 Administration
- Active Directory Domain Services (AD DS)
- Domain Controller Deployment
- Active Directory Forest Configuration
- DNS Integration
- Server Role Installation
- Enterprise Windows Administration

---

# Learning Outcome

After completing this task, I learned how to:

- Install Active Directory Domain Services
- Promote a server to a Domain Controller
- Create a new Active Directory forest
- Configure a new domain
- Configure Directory Services Restore Mode (DSRM)
- Validate a healthy Domain Controller installation
- Verify Active Directory and DNS functionality

---

# References

- Microsoft Learn – Active Directory Domain Services
- Microsoft Learn – Install a Domain Controller
- Windows Server 2016 Documentation

---

# Author

**Shamsur Rehman**

Windows Server 2016 Active Directory Lab

