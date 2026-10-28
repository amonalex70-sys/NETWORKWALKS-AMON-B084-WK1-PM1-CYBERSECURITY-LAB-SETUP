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


## ⚙️ Lab Configuration

| 🧩 Component       | ⚙️ Configuration   |
| ------------------ | ------------------  |
| 🖥️ Host OS         | Kali-Linux 2026.3       |
| 🧠 Host RAM        | 8 GB               |
| ⚡ Processor       | Intel Core i5   |
| 🧰 Virtualizaton Platform      | Oracle Virtualbox  |
| 🐉 Security OS     | Kali Linux 2026.2  |
| 🧠 Kali RAM        | 2048 MB (2GB)            |
| 🌐 Virtual Network | NAT Network        |
| 📡 Network Address | 10.0.0.0/24        |
| 🐧 Kali IP Address | 10.0.0.2/24        |
| 🚪 Default Gateway | 10.0.0.1           |
| 🌍 DNS Server      | 8.8.8.8            |
| 🔮 Future VM Range | 10.0.0.3–10.0.0.99 |

## ⚙️ Cybersecurity Lab Setup Steps

## Step 1: Install VirtualBox on Kali Linux

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




