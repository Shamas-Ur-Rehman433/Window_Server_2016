# Window_Server_2016
# Static IP Configuration

## Overview

This document explains how a static IPv4 address was configured on the Windows Server 2016 machine before installing Active Directory Domain Services (AD DS).

A static IP address is required because services such as Active Directory, DNS, and DHCP rely on a consistent network configuration. Unlike DHCP, a static IP address does not change after the server restarts.

---

# Objectives

- Configure a static IPv4 address
- Configure the subnet mask
- Configure the default gateway
- Configure the preferred DNS server
- Verify network connectivity
- Confirm the network configuration

---

# Prerequisites

Before configuring the static IP address, ensure the following:

- Windows Server 2016 is installed.
- The network adapter is connected.
- VMware Workstation or Hyper-V networking is configured (if using virtualization).
- The network topology has been planned.

---

# Environment

| Component | Value |
|-----------|-------|
| Operating System | Windows Server 2016 |
| Server Name | DC01 |
| Network Adapter | Ethernet |
| Network Type | Private Lab Network |

---

# Network Configuration

| Setting | Value |
|---------|-------|
| IP Address | 192.168.210.10 |
| Subnet Mask | 255.255.255.0 |
| Default Gateway | 192.168.210.1 |
| Preferred DNS Server | 192.168.210.10 |

---

# Procedure

## Step 1

Open **Control Panel**.

```
Control Panel

↓

Network and Internet

↓

Network and Sharing Center
```

---

## Step 2

Click:

```
Change Adapter Settings
```

---

## Step 3

Right-click the active network adapter.

```
Properties
```

---

## Step 4

Select:

```
Internet Protocol Version 4 (TCP/IPv4)

↓

Properties
```

---

## Step 5

Select:

```
Use the following IP address
```

Enter the following information:

| Field | Value |
|-------|-------|
| IP Address | 192.168.210.10 |
| Subnet Mask | 255.255.255.0 |
| Default Gateway | 192.168.210.1 |
| Preferred DNS Server | 192.168.210.10 |

Click **OK**.

---

## Step 6

Close all network configuration windows.

---

## Step 7

Open **Command Prompt**.

Run:

```cmd
ipconfig /all
```

Verify that all network settings have been applied successfully.

---

## Step 8

Test network connectivity.

Run:

```cmd
ping 192.168.210.1

ping 8.8.8.8

ping google.com
```

---

# Verification

Confirm the following:

- Static IP address is assigned.
- Subnet mask is correct.
- Default gateway is reachable.
- DNS server is configured.
- Internet connectivity is available.
- DNS name resolution is working.

---

# Screenshots

Store screenshots in:

```
Screenshots/02-Network/
```

Recommended screenshots:

- Network Adapter Settings
- Ethernet Properties
- IPv4 Configuration
- Static IP Configuration
- ipconfig /all Output
- Successful Ping to Gateway
- Successful Ping to 8.8.8.8
- Successful Ping to google.com

---

# Result

Successfully configured a static IPv4 address on the Windows Server 2016 machine.

The server can communicate with other devices on the network and is ready for the installation of Active Directory Domain Services (AD DS).

---

# Skills Demonstrated

- Windows Server Administration
- TCP/IP Configuration
- IPv4 Addressing
- Network Configuration
- DNS Configuration
- Network Troubleshooting

---

# Learning Outcome

After completing this task, I learned how to:

- Configure a static IP address
- Configure subnet masks and gateways
- Configure DNS settings
- Verify network connectivity
- Troubleshoot basic network issues using Command Prompt

---

# Commands Used

```cmd
ipconfig /all

ping 192.168.210.1

ping 8.8.8.8

ping google.com
```

---

# References

- Microsoft Learn – Configure TCP/IP Settings
- Windows Server 2016 Documentation

---

# Author

**Shamsur Rehman**

Windows Server 2016 Active Directory Lab

