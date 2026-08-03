# Window_Server_2016
# DNS Server Configuration

## Overview

This document explains how the **DNS Server** role was installed and configured on **Windows Server 2016**. The project includes creating a **Forward Lookup Zone**, **Reverse Lookup Zone**, and configuring common DNS resource records such as **A**, **CNAME**, **MX**, and **NS** records.

The DNS Server translates domain names into IP addresses, allowing users and devices to communicate using hostnames instead of numeric IP addresses. It is one of the core services required in an Active Directory environment.

---

# Objectives

- Install the DNS Server role
- Configure a Forward Lookup Zone
- Configure a Reverse Lookup Zone
- Create an A (Host) Record
- Create a CNAME (Alias) Record
- Create an MX (Mail Exchange) Record
- Create an NS (Name Server) Record
- Test DNS name resolution
- Verify DNS functionality

---

# Prerequisites

Before configuring the DNS Server, ensure the following:

- Windows Server 2016 is installed.
- A static IPv4 address is configured.
- The server has been promoted to a Domain Controller.
- Active Directory Domain Services (AD DS) is installed.
- Administrative privileges are available.

---

# Lab Environment

| Component | Value |
|-----------|-------|
| Operating System | Windows Server 2016 |
| Server Name | DC01 |
| Domain Name | gift.com |
| Server Role | DNS Server |
| IP Address | 192.168.210.10 |
| Preferred DNS | 192.168.210.10 |

---

# Network Configuration

| Setting | Value |
|---------|-------|
| IP Address | 192.168.210.10 |
| Subnet Mask | 255.255.255.0 |
| Default Gateway | 192.168.210.1 |
| Preferred DNS Server | 192.168.210.10 |

---

# DNS Installation

## Procedure

1. Open **Server Manager**.
2. Click **Manage** > **Add Roles and Features**.
3. Select **Role-based or feature-based installation**.
4. Select the local server.
5. Choose **DNS Server**.
6. Click **Add Features** when prompted.
7. Click **Install**.
8. Wait for the installation to complete.
9. Open **DNS Manager** from **Tools**.

---

# Forward Lookup Zone

## Configuration

Create a new Primary Zone.

| Setting | Value |
|---------|-------|
| Zone Type | Primary Zone |
| Zone Name | gift.com |
| Replication | To all DNS servers in the domain |
| Dynamic Updates | Secure Only |

The Forward Lookup Zone stores hostname-to-IP address mappings.

---

# Reverse Lookup Zone

## Configuration

Create a new IPv4 Reverse Lookup Zone.

| Setting | Value |
|---------|-------|
| Zone Type | Primary Zone |
| Network ID | 192.168.1 |
| Replication | To all DNS servers in the domain |
| Dynamic Updates | Secure Only |

The Reverse Lookup Zone resolves IP addresses back to hostnames.

---

# DNS Records

## A (Host) Record

The A Record maps a hostname to an IPv4 address.

Example:

| Hostname | IP Address |
|----------|------------|
| dc01 | 192.168.210.10 |
| server01 | 192.168.210.20 |

---

## CNAME (Alias) Record

The CNAME Record creates an alias for an existing host.

Example:

| Alias | Target Host |
|-------|-------------|
| www | dc01.gift.com |

---

## MX (Mail Exchange) Record

The MX Record specifies the mail server responsible for receiving email.

Example:

| Mail Server | Priority |
|-------------|----------|
| mail.company.local | 10 |

---

## NS (Name Server) Record

The NS Record identifies the authoritative DNS server for the domain.

Example:

| Name Server |
|-------------|
| dc01.gift.com |

---

# DNS Testing

After configuration, verify DNS functionality using the following commands.

```cmd
ipconfig /all

ipconfig /displaydns

nslookup gift.com

nslookup dc01

ping gift.com

ping dc01
```

Verify that:

- DNS resolves hostnames correctly.
- Ping succeeds using hostnames.
- `nslookup` returns the correct IP address.
- The DNS cache contains the expected records.

---

# Verification Checklist

- DNS Server role installed successfully.
- Forward Lookup Zone created.
- Reverse Lookup Zone created.
- A Record configured.
- CNAME Record configured.
- MX Record configured.
- NS Record configured.
- DNS name resolution working correctly.
- Client computers can resolve domain names.

---

# Screenshots

Store screenshots in the following folders:

```
Screenshots/
│
├── 01-DNS-Installation
├── 02-Forward-Lookup-Zone
├── 03-Reverse-Lookup-Zone
├── 04-A-Record
├── 05-CNAME-Record
├── 06-MX-Record
├── 07-NS-Record
├── 08-DNS-Testing
└── 09-Final-Verification
```

Recommended screenshots:

- DNS Server installation
- DNS Manager
- Forward Lookup Zone
- Reverse Lookup Zone
- A Record
- CNAME Record
- MX Record
- NS Record
- `ipconfig /all`
- `nslookup gift.com`
- `nslookup dc01`
- `ping gift.com`
- `ping dc01`
- Final DNS Manager showing all configured records

---

# Result

Successfully installed and configured the **DNS Server** role on Windows Server 2016. Created both Forward and Reverse Lookup Zones, configured common DNS resource records, and verified successful hostname resolution using DNS diagnostic tools.

---

# Skills Demonstrated

- Windows Server 2016 Administration
- DNS Server Installation
- DNS Zone Configuration
- Forward Lookup Zone Management
- Reverse Lookup Zone Management
- A Record Configuration
- CNAME Record Configuration
- MX Record Configuration
- NS Record Configuration
- DNS Name Resolution
- Command-Line Troubleshooting
- Enterprise Network Administration

---

# Learning Outcome

After completing this project, I learned how to:

- Install and configure the DNS Server role.
- Create and manage Forward and Reverse Lookup Zones.
- Configure commonly used DNS resource records.
- Test DNS functionality using built-in Windows networking tools.
- Troubleshoot DNS name resolution issues.
- Understand the importance of DNS in an Active Directory environment.

---

# References

- Microsoft Learn – DNS Server Overview
- Microsoft Learn – Windows Server DNS Documentation
- Microsoft Learn – Active Directory Domain Services

---

# Author

**Shamsur Rehman**

Windows Server 2016 DNS Server Lab