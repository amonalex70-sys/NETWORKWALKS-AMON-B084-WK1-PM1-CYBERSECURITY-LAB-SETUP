<div align="center">
  
# Cybersecurity Lab Setup and Configuration
Setting up a cybersecurity lab for hands-on security practice and learning.


<p align="center">
  <img src="https://img.shields.io/badge/Project-Cybersecurity%20Lab-404040?style=flat-square&labelColor=C00000" />
  <img src="https://img.shields.io/badge/VirtualBox-v7.2-0070C0?style=flat-square&labelColor=000000" />
  <img src="https://img.shields.io/badge/Kali%20Linux-v2026.2-E87500?style=flat-square&labelColor=000000&logo=kalilinux&logoColor=white" />
  <img src="https://img.shields.io/badge/Operating%20System-Linux-404040?style=flat-square&labelColor=C00000" />
  <img src="https://img.shields.io/badge/Network-10.0.0.0%2F24-238F89?style=flat-square&labelColor=000000" />
  <img src="https://img.shields.io/badge/Focus-Penetration%20Testing-C00000?style=flat-square&labelColor=000000&logo=kalilinux&logoColor=white" />
  <img src="https://img.shields.io/badge/Technology-Virtualization-404040?style=flat-square&labelColor=C00000" />
  <img src="https://img.shields.io/badge/Platform-GitHub-404040?style=flat-square&labelColor=0070C0&logo=github&logoColor=white" />
  <img src="https://img.shields.io/badge/Distribution-Kali%20Linux-404040?style=flat-square&labelColor=C00000&logo=kalilinux&logoColor=white" />
  <img src="https://img.shields.io/badge/Program-NetworkWalks-404040?style=flat-square&labelColor=C00000" />
  <img src="https://img.shields.io/badge/Practice-Ethical%20Hacking-E87500?style=flat-square&labelColor=000000&logo=kalilinux&logoColor=white" />
  <img src="https://img.shields.io/badge/Mentor-Waqas%20Karim%20(CCIE)-C00000?style=flat-square" />
</p>
</div>

## 🛡️ Cybersecurity Lab Setup and Overview

This project documents the setup of a **virtual cybersecurity lab** using VirtualBox and Kali Linux to practice network security, reconnaissance, penetration testing, and vulnerability assessment in a controlled environment.

The lab uses a private virtual network to support future expansion, allowing additional virtual machines to be added for safe, isolated, and authorized security testing.

## 🎯 Lab Setup Objectives

The primary objectives of this project are to:

- Install and configure VirtualBox for virtualization.
- Deploy Kali Linux as a virtual machine.
- Create a private NAT Network for the lab environment.
- Configure network connectivity and assign a consistent IP address to Kali Linux.
- Verify network connectivity and DNS resolution.
- Create a clean virtual machine snapshot for recovery.
- Document the installation and configuration process.
- Establish a foundation for future cybersecurity and penetration-testing projects.



## 🛡️ Lab Purpose and Security Scope

This lab provides an isolated and controlled environment for cybersecurity training, practical learning, and authorized security testing.

It supports hands-on practice in the following areas:

- Network reconnaissance and port scanning
- Vulnerability assessment
- Network traffic and packet analysis
- Web application security testing
- Exploitation techniques in a controlled environment
- Cybersecurity tool installation, configuration, and testing

**⚠️ Security Notice:** All testing must be conducted on systems you own or have explicit permission to assess. Never target unauthorized systems or networks.


## ⚙️ Cybersecurity Lab System Specifications

| 🧩 Component       | ⚙️ Configuration   |
| ------------------ | ------------------  |
| 🖥️ Host OS         | Kali-Linux 2026.3       |
| 🧠 Host RAM        | 8 GB               |
| ⚡ Processor       | Intel Core i5   |
| 🧰 Virtualizaton Platform      | Oracle Virtualbox v7.2.20  |
| 🐉 Security OS     | Kali Linux 2026.3  |
| 🧠 Kali RAM        | 2048 MB (2GB)            |
| 🌐 Virtual Network | NAT Network        |
| 📡 Network Address | 10.0.0.0/24        |
| 🐧 Kali IP Address | 10.0.0.2/24        |
| 🚪 Default Gateway | 10.0.0.1           |
| 🌍 DNS Server      | 8.8.8.8            |
| 🔮 Future VM Range | 10.0.0.3–10.0.0.99 |

## ⚙️ Cybersecurity Lab Setup Steps

## Step 1: Install 7-Zip on Kali Linux

The `p7zip-full` package was installed using the APT package manager to enable extraction of the downloaded Kali Linux virtual-machine archive in `.7z` format.

**Tool:** 7-Zip (`p7zip-full`)

**Installation command:**
```bash
sudo apt update
sudo apt install p7zip-full -y
```

---
## Step 2: Install VirtualBox on Kali Linux

VirtualBox was installed on the Kali Linux host system using the APT package manager and the official Kali Linux repositories.

**Installation commands:**

```bash
sudo apt update
sudo apt install virtualbox linux-headers-generic
```

**Verify the installation:**

```bash
virtualbox --help
```

**Official documentation:** [Installing VirtualBox on Kali Linux](https://www.kali.org/docs/virtualization/install-virtualbox-host/)

## Step 3: Create and Configure the NAT Network

A dedicated NAT Network was configured in Oracle VirtualBox to provide network connectivity for the cybersecurity lab.

**Configuration:**

| Component | Setting |
|---|---|
| Network Name | `NatNetwork` |
| IPv4 Prefix | `10.0.0.0/24` |
| DHCP | Enabled |
| IPv6 | Disabled |

The NAT Network provides internet access to connected virtual machines and allows communication between them within the configured virtual network.

## Step 4: Import Kali Linux into VirtualBox

The prebuilt Kali Linux virtual-machine image was downloaded from the official Kali Linux website and extracted using 7-Zip. The extracted `.vbox` configuration file was opened in VirtualBox to load the virtual machine's predefined settings.

**The VM network adapter configurations**
```text
Network Adapter: Adapter 1 
Network Mode: NAT Network 
Network Name: `NatNetwork` 
Adapter Type: Intel PRO/1000 MT Desktop 
```

## Step 5: Configure the Kali Linux Network

The Kali Linux network settings were configured to use a consistent IPv4 address within the lab's NAT Network.

**Network Configuration**

```text
IP Address:    10.0.0.2/24
Subnet Mask:   255.255.255.0
Default Gateway: 10.0.0.1
DNS Server:    8.8.8.8
```

Using a consistent IP address simplifies network identification, troubleshooting, and documentation for future cybersecurity lab exercises.

<img width="1271" height="756" alt="Network configuration " src="https://github.com/user-attachments/assets/190b4936-0c2c-48d8-988b-b2e45f3474e9"/>

## Step 6: Create a Clean VM Snapshot

A snapshot was created in Oracle VirtualBox to preserve the initial Kali Linux setup and provide a recovery point for future cybersecurity experiments.

**Snapshot Name:**

```text
`Clean kali - Network setup`
```

## 🔎 Step 7: Lab Verification

| ✅ Test                        | 🧾 Command                      | 🎯 Expected Result              |
| ----------------------------- | ------------------------------- | ------------------------------- |
| 🌐 Check IP address           | `ip addr`                          | Correct Kali IP displayed       |
| 📡 Test gateway               | `ping 10.0.0.1`                 | Successful replies              |
| 🌍 Test Internet connectivity | `ping 4 8.8.8.8`                  | Successful replies              |
| 🔎 Test DNS resolution        | `nslookup networkwalks.com`     | Domain resolves                 |
| 🧰 Verify Nmap                | `nmap --version`                | Nmap version displayed          |
| 🔄 Verify snapshot            | Restore snapshot and run `ip a` | Baseline configuration restored |

Verification result test:

<img width="690" height="614" alt="Verification test" src="https://github.com/user-attachments/assets/c4f0991f-17a9-41c5-b1a8-f5c9422637c1" />


# 🐞 Problems Encountered & Solutions

Documenting troubleshooting steps helps improve the lab setup and supports future reference.

## Problem 1: Internet Connectivity After Static IP Configuration

After configuring a static IPv4 address, internet connectivity may fail due to network configuration issues.

**Solution:** The following NetworkManager setting was applied as a workaround during the lab:

```bash
sudo nmcli connection modify "Wired connection 1" ipv4.dad-timeout 0
```

The network connection was restarted, and internet connectivity was tested again.

> **Note:** Connection names vary between systems. Identify the correct connection name before executing the command.

# 💡 What I Learned

Through this project, I learned how to create and configure a virtual environment for cybersecurity practice using Kali Linux and Oracle VirtualBox.

The most important concepts I learned include:

### 1. Virtualization and VM Configuration

I learned how to install VirtualBox, extract a prebuilt Kali Linux virtual machine, open its `.vbox` configuration file, and configure essential resources such as RAM and network adapters.

### 2. NAT vs NAT Network

I learned the difference between standard NAT and NAT Network. A NAT Network allows multiple connected virtual machines to communicate with one another while providing network address translation for external connectivity.

### 3. Virtual Machine Networking

I learned how to configure VirtualBox network adapters, select the appropriate network mode, and understand settings such as promiscuous mode and cable connection.

### 4. Static IP Configuration

I learned how to configure and verify IPv4 addresses, subnet masks, default gateways, and DNS settings in Kali Linux. I also gained experience troubleshooting internet connectivity issues related to network configuration.

### 5. VM Snapshots

I learned how to create a clean snapshot in VirtualBox to preserve a working Kali Linux configuration. This provides a recovery point before performing risky or experimental cybersecurity activities.

### 6. Troubleshooting and Documentation

I learned how to investigate network connectivity problems, apply configuration changes, test connectivity, and document commands, screenshots, problems, and solutions in a structured GitHub repository.

### 7. Cybersecurity Lab Preparation

I established a foundation for future hands-on exercises involving network reconnaissance, packet analysis, vulnerability assessment, and authorized penetration testing within a controlled virtual environment.

---

# 🔐 Security & Ethical Use

This laboratory is intended strictly for educational purposes. All cybersecurity activities must be conducted in a controlled environment and only on systems you own or have explicit authorization to test.

---

# 🔗 Tools & Resources

- **7-Zip:** https://www.7-zip.org/download.html
- **VirtualBox:** https://www.virtualbox.org/wiki/Downloads
- **Kali Linux:** https://www.kali.org/get-kali/

---

# 👤 Author

**Amon Alex**  
Cybersecurity Student | Electronics, Telecommunications & Cybersecurity

**LinkedIn:** [Amon Alex](https://www.linkedin.com/in/amon-lowasa-60877a42a/)


## 📌 Project Information

**Program Name:** Cybersecurity at Networkwalks | **Week:** 01 | **Project:** Cybersecurity & Pentesting Lab Setup | **Repository:** GitHub

