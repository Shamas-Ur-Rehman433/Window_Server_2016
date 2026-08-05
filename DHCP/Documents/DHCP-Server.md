# Windows Server 2016 – DHCP Server Lab

## Overview

This project demonstrates the installation and configuration of the **Dynamic Host Configuration Protocol (DHCP)** Server role on **Windows Server 2016**. It covers the complete DHCP deployment process, including creating a DHCP scope, configuring an exclusion range, creating reservations, modifying the lease duration, and verifying automatic IP address assignment on a client computer.

This project is intended to demonstrate practical Windows Server administration skills in a lab environment.

---

# Objectives

* Install the DHCP Server role.
* Complete the post-installation configuration.
* Authorize the DHCP Server in Active Directory.
* Create and activate a DHCP scope.
* Configure an exclusion range.
* Create DHCP reservations.
* Configure the lease duration.
* Verify automatic IP address assignment.
* Test DHCP functionality using Windows networking commands.

---

# Lab Environment

| Component               | Configuration                 |
| ----------------------- | ----------------------------- |
| Operating System        | Windows Server 2016           |
| Server Name             | DC01                          |
| Domain Name             | gift.com                 |
| Server IP Address       | 192.168.210.10                  |
| DHCP Scope              | 192.168.210.100 – 192.168.210.200 |
| Client Operating System | Windows 10 / Windows 11       |

---

# Features Implemented

* DHCP Server Installation
* DHCP Post-Installation Configuration
* DHCP Server Authorization
* IPv4 Scope Creation
* Address Pool Configuration
* Exclusion Range Configuration
* DHCP Reservation
* Lease Duration Configuration
* Automatic IP Address Assignment
* DHCP Testing and Verification

---

# Screenshots Included

## 1. DHCP Installation

* Server Manager
* Add Roles and Features Wizard
* DHCP Server Role Selected
* Add Features
* Installation Completed
* DHCP Manager

---

## 2. DHCP Configuration

* Post-Installation Configuration
* DHCP Authorization
* DHCP Console

---

## 3. New Scope

* New Scope Wizard
* Scope Name
* IP Address Range
* Subnet Mask
* Default Gateway
* DNS Configuration
* Scope Activation
* Scope Created Successfully

---

## 4. Exclusion Range

* New Exclusion Range
* Exclusion Range Configured
* Exclusion List

---

## 5. Reservation

* New Reservation
* MAC Address Configuration
* Reservation Created
* Reservation List

---

## 6. Lease Duration

* Lease Duration Settings
* Lease Duration Configured

---

## 7. DHCP Testing

The following commands were executed to verify DHCP functionality:

```cmd
ipconfig /all
ipconfig /release
ipconfig /renew
ping dc01
ping company.local
```

---

## 8. Final Verification

The final DHCP Manager screenshot confirms:

* DHCP Server
* IPv4
* Address Pool
* Address Leases
* Reservations
* Scope Options
* Active Scope

---

# Result

The DHCP Server was successfully installed and configured on Windows Server 2016. Client computers were able to obtain IP addresses automatically from the configured DHCP scope. Reservations, exclusion ranges, and lease duration settings were verified successfully.

---

# Skills Demonstrated

* Windows Server 2016 Administration
* DHCP Server Installation
* DHCP Server Authorization
* DHCP Scope Configuration
* Address Pool Management
* Exclusion Range Configuration
* DHCP Reservation
* Lease Duration Management
* TCP/IP Configuration
* Client Network Configuration
* Network Troubleshooting
* Enterprise Windows Server Administration

---

# Learning Outcomes

After completing this project, I learned how to:

* Install and configure the DHCP Server role.
* Authorize a DHCP Server in an Active Directory environment.
* Create and manage DHCP scopes.
* Configure exclusion ranges and reservations.
* Manage DHCP lease duration.
* Verify automatic IP address assignment.
* Troubleshoot DHCP-related issues using Windows networking tools.

---

# Author

**Shamsur Rehman**

**Windows Server 2016 – DHCP Server Lab**
