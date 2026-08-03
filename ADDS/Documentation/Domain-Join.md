# Window_Server_2016
# Domain Join

## Overview

This document explains how a Windows client computer was joined to the **company.local** Active Directory domain in the Windows Server 2016 Active Directory Domain Services (AD DS) Lab.

Joining a client computer to a domain allows centralized authentication, user management, Group Policy application, and secure access to network resources. Instead of using local user accounts, users can log in with their domain credentials from any domain-joined computer.

---

# Objectives

- Configure the client computer
- Verify network connectivity
- Join the client computer to the Active Directory domain
- Restart the client computer
- Log in using a domain user account
- Verify successful domain membership

---

# Prerequisites

Before joining the client computer to the domain, ensure the following:

- Windows Server 2016 is configured as a Domain Controller.
- Active Directory Domain Services (AD DS) is installed.
- The domain **company.local** has been created.
- DNS is functioning correctly.
- The client computer can communicate with the Domain Controller.
- The client computer is configured to use the Domain Controller as its preferred DNS server.

---

# Environment

| Component | Value |
|-----------|-------|
| Domain Controller | DC01 |
| Operating System | Windows Server 2016 |
| Client Operating System | Windows 10 / Windows 11 |
| Domain Name | company.local |
| Management Tool | System Properties |

---

# Network Configuration

## Domain Controller

| Setting | Value |
|---------|-------|
| IP Address | 192.168.210.10 |
| Preferred DNS | 192.168.210.10 |

---

## Client Computer

| Setting | Value |
|---------|-------|
| IP Address | 192.168.210.20 |
| Subnet Mask | 255.255.255.0 |
| Default Gateway | 192.168.210.1 |
| Preferred DNS | 192.168.210.10 |

---

# Procedure

## Step 1

Verify the client's network configuration.

Run:

```cmd
ipconfig /all
```

Confirm that the Preferred DNS Server points to the Domain Controller.

---

## Step 2

Verify network connectivity.

Run:

```cmd
ping 192.168.210.10

ping gift.local
```

Ensure both commands return successful replies.

---

## Step 3

Open **System Properties**.

Navigate to:

```
This PC

↓

Properties

↓

Advanced System Settings

↓

Computer Name

↓

Change
```

---

## Step 4

Select:

```
Domain
```

Enter the domain name:

```
gift.local
```

Click **OK**.

---

## Step 5

When prompted, enter the credentials of a domain administrator.

Example:

| Field | Value |
|-------|-------|
| Username | company\Administrator |
| Password | ******** |

> **Note:** Never publish passwords in GitHub repositories.

---

## Step 6

Wait for the confirmation message.

```
Welcome to the company.local domain.
```

Click **OK**.

---

## Step 7

Restart the client computer.

---

## Step 8

At the login screen, choose:

```
Other User
```

Log in using a domain account.

Example:

```
gift\alikhan
```

or

```
alikhan
```

Enter the user's password and sign in.

---

# Verification

Confirm the following:

- The client computer is joined to the domain.
- The computer appears in **Active Directory Users and Computers**.
- Domain users can successfully log in.
- The client can communicate with the Domain Controller.
- DNS name resolution is functioning correctly.

---

# Screenshots

Store screenshots in:

```
Screenshots/07-Client-Join/
```

Recommended screenshots:

- Client Network Configuration
- ipconfig /all Output
- Successful Ping to Domain Controller
- Computer Name Window
- Domain Join Dialog
- Domain Administrator Credentials Prompt (hide the password)
- Welcome to the Domain Message
- Restart Prompt
- Domain Login Screen
- Successful Domain User Login
- Computer Object in Active Directory Users and Computers

---

# Result

Successfully joined the Windows client computer to the **company.local** Active Directory domain.

The client is now centrally managed by the Domain Controller and can authenticate users using Active Directory accounts.

---

# Benefits of Domain Join

- Centralized user authentication
- Centralized user management
- Group Policy enforcement
- Improved security
- Simplified administration
- Access to shared network resources
- Single sign-on (SSO) within the domain

---

# Skills Demonstrated

- Windows Server Administration
- Active Directory Domain Services
- Domain Management
- DNS Configuration
- Client Administration
- Network Troubleshooting
- Enterprise Windows Administration

---

# Learning Outcome

After completing this task, I learned how to:

- Configure a client computer for domain connectivity
- Verify DNS and network communication
- Join a Windows client to an Active Directory domain
- Authenticate using domain credentials
- Verify domain membership
- Troubleshoot common domain join issues

---

# Commands Used

```cmd
ipconfig /all

ping 192.168.210.10

ping gift.local
```

---

# References

- Microsoft Learn – Join a Computer to an Active Directory Domain
- Windows Server 2016 Documentation

---

# Author

**Shamsur Rehman**

Windows Server 2016 Active Directory Lab

