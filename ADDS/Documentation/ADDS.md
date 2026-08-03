# Window_Server_2016
# Active Directory Domain Services (AD DS)

## Overview

This document explains the installation of **Active Directory Domain Services (AD DS)** on Windows Server 2016.

Active Directory Domain Services is a Windows Server role that provides centralized management of users, computers, groups, organizational units (OUs), and security policies within a Windows domain. Installing AD DS is the first step before promoting a server to a Domain Controller.

---

# Objectives

- Install the Active Directory Domain Services role
- Add the required management tools
- Prepare the server for Domain Controller promotion
- Verify successful installation
- Understand the purpose of AD DS

---

# Prerequisites

Before installing AD DS, ensure the following:

- Windows Server 2016 is installed.
- A static IPv4 address is configured.
- The server has been renamed to **DC01**.
- Network connectivity is verified.
- The server is logged in with an Administrator account.

---

# Environment

| Component | Value |
|-----------|-------|
| Operating System | Windows Server 2016 |
| Server Name | DC01 |
| Server Role | Member Server |
| Feature | Active Directory Domain Services |
| Installation Method | Server Manager |

---

# Procedure

## Step 1

Open **Server Manager**.

---

## Step 2

Click:

```
Manage

↓

Add Roles and Features
```

---

## Step 3

In the **Before You Begin** window, click:

```
Next
```

---

## Step 4

Select:

```
Role-based or feature-based installation
```

Click **Next**.

---

## Step 5

Select the local server.

Example:

```
DC01
```

Click **Next**.

---

## Step 6

From the list of server roles, select:

```
Active Directory Domain Services
```

When prompted, click:

```
Add Features
```

The following management tools will also be installed automatically:

- Active Directory Administrative Center
- Active Directory Module for Windows PowerShell
- Active Directory Users and Computers
- Active Directory Sites and Services
- Active Directory Domains and Trusts

Click **Next**.

---

## Step 7

Review the **Features** page.

No additional features are required.

Click **Next**.

---

## Step 8

Review the **Active Directory Domain Services** information page.

Click **Next**.

---

## Step 9

Click:

```
Install
```

Wait for the installation to complete.

---

## Step 10

After the installation finishes, verify that the following message appears:

```
Configuration required.

Promote this server to a domain controller.
```

Do **not** promote the server yet if you are documenting the installation separately.

---

# Verification

Verify the following:

- Installation completed successfully.
- No installation errors are reported.
- The notification flag appears in Server Manager.
- "Promote this server to a domain controller" is available.
- Active Directory management tools are installed.

---

# Validation

Open **Server Manager**.

Verify that **Active Directory Domain Services** appears under the installed roles.

Open:

```
Tools
```

Confirm the following management tools are available:

- Active Directory Users and Computers
- Active Directory Administrative Center
- Active Directory Domains and Trusts
- Active Directory Sites and Services

---

# Screenshots

Store screenshots in:

```
Screenshots/02-ADDS/
```

Recommended screenshots:

- Server Manager Dashboard
- Add Roles and Features Wizard
- Server Selection
- Server Roles Page
- Active Directory Domain Services Selected
- Add Features Dialog Box
- Features Page
- AD DS Information Page
- Tools Menu Showing AD Management Tools

---

# Result

Successfully installed the **Active Directory Domain Services (AD DS)** role on Windows Server 2016.

The server is now prepared for promotion to a Domain Controller and is ready for Active Directory forest and domain configuration.

---

# Benefits of Active Directory Domain Services

- Centralized user management
- Centralized computer management
- Authentication and authorization
- Organizational Unit (OU) management
- Group Policy support
- Security management
- Scalability for enterprise networks
- Integration with DNS

---

# Skills Demonstrated

- Windows Server 2016 Administration
- Server Role Installation
- Active Directory Domain Services
- Server Manager
- Windows Feature Management
- Enterprise Infrastructure Setup

---

# Learning Outcome

After completing this task, I learned how to:

- Install the Active Directory Domain Services role
- Add the required AD management tools
- Verify a successful role installation
- Prepare a Windows Server for Domain Controller promotion
- Understand the purpose of AD DS in an enterprise environment

---

# References

- Microsoft Learn – Active Directory Domain Services Overview
- Microsoft Learn – Install Active Directory Domain Services
- Windows Server 2016 Documentation

---

# Author

**Shamsur Rehman**

Windows Server 2016 Active Directory Lab
