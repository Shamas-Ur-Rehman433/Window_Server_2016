# Window_Server_2016
# Organizational Units (OU)

## Overview

This document explains how Organizational Units (OUs) were created and managed in the **Windows Server 2016 Active Directory Domain Services (AD DS) Lab**.

Organizational Units are logical containers within Active Directory used to organize users, computers, groups, and other objects. OUs simplify administration by allowing administrators to delegate control and apply Group Policy Objects (GPOs) to specific departments.

---

# Objectives

- Create Organizational Units (OUs)
- Organize Active Directory objects
- Prepare the environment for Group Policy
- Improve administrative management
- Build a structured Active Directory hierarchy

---

# Prerequisites

Before creating Organizational Units, ensure the following:

- Windows Server 2016 is installed.
- Active Directory Domain Services (AD DS) is installed.
- The server has been promoted to a Domain Controller.
- A domain has been successfully created.

---

# Environment

| Component | Value |
|-----------|-------|
| Operating System | Windows Server 2016 |
| Server Name | DC01 |
| Domain | company.local |
| Management Tool | Active Directory Users and Computers (ADUC) |

---

# Organizational Structure

```
company.local
│
└── Company
    │
    ├── IT
    ├── HR
    ├── Finance
    ├── Accounts
    ├── Sales
    ├── Management
    └── Support
```

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

Expand the domain.

```
gift.local
```

---

## Step 4

Right-click the domain.

```
New

↓

Organizational Unit
```

---

## Step 5

Create the parent Organizational Unit.

Example:

| Field | Value |
|-------|-------|
| Name | Company |

Click **OK**.

---

## Step 6

Right-click the **Company** OU.

```
New

↓

Organizational Unit
```

---

## Step 7

Create the following child Organizational Units:

| Organizational Unit |
|---------------------|
| IT |
| HR |
| Finance |
| Accounts |
| Sales |
| Management |
| Support |

---

## Step 8

Verify that all Organizational Units appear under the **Company** OU.

---

# Verification

Confirm the following:

- The Company OU exists.
- All department OUs are created.
- No duplicate Organizational Units exist.
- The OU hierarchy is correct.

---

# Screenshots

Store screenshots in:

```
Screenshots/04-OU/
```

Recommended screenshots:

- Active Directory Users and Computers
- Creating the Company OU
- Creating a Department OU
- Complete OU Structure
- Final Organizational Hierarchy

---

# Result

Successfully created Organizational Units within the **company.local** domain.

The Active Directory environment is now organized into departmental containers, making user, computer, and group management easier and preparing the domain for Group Policy deployment.

---

# Benefits of Organizational Units

- Organizes Active Directory objects
- Simplifies administration
- Makes user management easier
- Supports Group Policy deployment
- Allows delegation of administrative control
- Improves scalability for enterprise environments

---

# Skills Demonstrated

- Active Directory Administration
- Organizational Unit Management
- Windows Server Administration
- Enterprise Directory Structure
- Active Directory Planning

---

# Learning Outcome

After completing this task, I learned how to:

- Create Organizational Units
- Design an enterprise Active Directory structure
- Organize departments within a domain
- Prepare Active Directory for Group Policy Objects (GPOs)
- Improve directory management using OUs

---

# References

- Microsoft Learn – Active Directory Organizational Units
- Windows Server 2016 Documentation

---

# Author

**Shamsur Rehman**

Windows Server 2016 Active Directory Lab

