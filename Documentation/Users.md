# Window_Server_2016
# Active Directory User Management

## Overview

This document explains how Active Directory user accounts were created and managed in the **Windows Server 2016 Active Directory Domain Services (AD DS) Lab**.

The purpose of creating user accounts is to provide authentication, authorization, and centralized identity management for users within the domain.

---

# Objectives

- Create Active Directory user accounts
- Assign users to Organizational Units (OUs)
- Configure user properties
- Set passwords
- Enable user accounts
- Verify successful user creation

---

# Prerequisites

Before creating users, the following must already be configured:

- Windows Server 2016 installed
- Active Directory Domain Services (AD DS) installed
- Server promoted to a Domain Controller
- Domain successfully created
- Organizational Units (OUs) created

---

# Environment

| Component | Value |
|-----------|-------|
| Operating System | Windows Server 2016 |
| Domain | gift.local |
| Server Name | DC01 |
| Tool Used | Active Directory Users and Computers (ADUC) |

---

# Users Created

| Name | Username | Department |
|------|----------|------------|
| Ali Khan | alikhan | IT |
| Ahmed Raza | ahmedraza | HR |
| Sara Ali | saraali | Finance |
| John Smith | johnsmith | Sales |
| David Lee | davidlee | Support |
| Usama Hafeez | usamahafeez | Account |
| Nasir Zahid | nasirzahid | Management |

---

# Procedure

## Step 1

Open **Server Manager**.

---

## Step 2

Navigate to:

```
Tools

↓

Active Directory Users and Computers
```

---

## Step 3

Select the appropriate Organizational Unit (OU).

Example:

```
Company

↓

IT
```

---

## Step 4

Right-click the Organizational Unit.

```
New

↓

User
```

---

## Step 5

Enter the user information.

Example:

| Field | Value |
|-------|-------|
| First Name | Ali |
| Last Name | Khan |
| User Logon Name | alikhan |

Click **Next**.

---

## Step 6

Configure the password.

Example:

- Password: ********
- Confirm Password: ********

Options:

- User must change password at next logon
- User cannot change password
- Password never expires
- Account is disabled

> 

Click **Next**.

---

## Step 7

Click **Finish** to create the user account.

---

# Verification

Verify that:

- User appears in the selected Organizational Unit.
- Username is correct.
- Account is enabled.
- User can log in to the domain.

---

# Screenshots

Store screenshots in:

```
Screenshots/05-Users/
```

Recommended screenshots:

- Active Directory Users and Computers
- Selected Organizational Unit

---

# Result

Successfully created Active Directory user accounts within the **gift.local** domain.

All users were placed in their respective Organizational Units and are ready for authentication and resource access.

---

# Skills Demonstrated

- Active Directory Administration
- User Account Management
- Organizational Unit Management
- Domain Administration
- Identity Management
- Windows Server Administration

---

# Learning Outcome

After completing this task, I learned how to:

- Create Active Directory users
- Configure user properties
- Assign users to Organizational Units
- Manage user passwords
- Verify user accounts
- Perform basic identity management in Active Directory

---

# References

- Microsoft Learn – Active Directory Domain Services
- Windows Server 2016 Documentation

---

**Author**

**Shamsur Rehman**

Windows Server 2016 Active Directory Lab

