
<div align="center">

 #🔐 Cybersecurity Lab Environment Setup

**Building an isolated virtual lab for penetration testing and ethical hacking practice**
</div>

<p align="center">
  <img src="https://img.shields.io/badge/Skill-Cybersecurity-404040?style=flat-square&labelColor=C00000" />
  <img src="https://img.shields.io/badge/Ver-Virtualbox%20v7.2-0070C0?style=flat-square&labelColor=000000" />
  <img src="https://img.shields.io/badge/Kali%20Linux-v2026.2-E87500?style=flat-square&labelColor=000000&logo=kalilinux&logoColor=white" />
  <img src="https://img.shields.io/badge/Skill-Linux-404040?style=flat-square&labelColor=C00000" />
  <img src="https://img.shields.io/badge/Network-10.0.0.0%2F24-238F89?style=flat-square&labelColor=000000" />
  <img src="https://img.shields.io/badge/Penetration%20Testing-C00000?style=flat-square&labelColor=000000&logo=kalilinux&logoColor=white" />
  <img src="https://img.shields.io/badge/Skill-Virtualization-404040?style=flat-square&labelColor=C00000" />
  <img src="https://img.shields.io/badge/GitHub-404040?style=flat-square&labelColor=0070C0&logo=github&logoColor=white" />
  <img src="https://img.shields.io/badge/Kali%20Linux-404040?style=flat-square&labelColor=C00000&logo=kalilinux&logoColor=white" />
  <img src="https://img.shields.io/badge/NetworkWalks-404040?style=flat-square&labelColor=C00000" />
  <img src="https://img.shields.io/badge/Ethical%20Hacking-E87500?style=flat-square&labelColor=000000&logo=kalilinux&logoColor=white" />
  <img src="https://img.shields.io/badge/Waqas%20Karim%20CCIE-C00000?style=flat-square" />
</p># 🔐 Cybersecurity Lab Setup

## 📌 Overview
This project involves setting up a virtual cybersecurity lab using Kali Linux and Oracle VirtualBox. The lab provides an environment for learning network configuration, reconnaissance, and ethical hacking techniques.

## 🎯 Objectives

The main objectives of this project are to:

- Install and configure VirtualBox.
- Install/import Kali Linux as a virtual machine.
- Create a private **NAT Network** for the cybersecurity lab.
- Configure network connectivity for Kali Linux.
- Assign a consistent IP address to the Kali VM.
- Verify network connectivity and DNS resolution.
- Take a clean VM snapshot for recovery.
- Document the complete setup process.
- Prepare the environment for future cybersecurity projects.
- ## 🛡️ Purpose of the Lab

The lab provides an isolated and controlled environment for cybersecurity learning and authorized security testing.

It can be used for activities such as:

- Network reconnaissance
- Port scanning
- Vulnerability assessment
- Packet analysis
- Web security testing
- Exploitation practice
- Security-tool experimentation
- ⚠️ **Important:** This laboratory must only be used for systems that you own or have explicit permission to test. Do not use the lab or its tools to attack unauthorized systems.
- ## 🏗️ Lab Architecture
<img width="1357" height="609" alt="image" src="https://github.com/user-attachments/assets/af710fe5-9b0c-4f6b-9286-3f20cd6f9102" />
## 🛠️ Tools Used
- Kali Linux
- Oracle VirtualBox
- Nmap
- Wireshark
- Windows

## 🏗️ Lab Configuration

| Component | Configuration |
|---|---|
| Host OS | Windows |
| Virtualization | Oracle VirtualBox |
| Virtual Machine | Kali Linux |
| Network Mode | NAT Network |
| IPv4 Subnet | 10.0.0.0/24 |

*Update these values to match your actual configuration.*
# 🪜 Lab Setup Procedure

## Step 1. Install 7-Zip

7-Zip was installed to extract the Kali Linux virtual-machine package, which may be distributed as a `.7z` archive.

**Tool:** 7-Zip

---
## Step 2. Install VirtualBox

VirtualBox was installed as the hypervisor.
<img width="1360" height="768" alt="image" src="https://github.com/user-attachments/assets/19b802b2-b352-4f00-b7e9-24dfbc77f360" />

---
## Step 3. Create the NAT Network

A dedicated NAT Network was created in VirtualBox.

Configuration:
Network Name: NatNetwork
IPv4 Prefix:  10.0.0.0/24
DHCP:         Enabled
IPv6:         Disabled
<img width="1360" height="768" alt="image" src="https://github.com/user-attachments/assets/dbff1956-8ac0-42cf-a243-3ff053629961" />


A **NAT Network** was selected because multiple virtual machines connected to the same NAT Network can communicate with one another while also having outbound network connectivity.

This will allow future attacker and target VMs to communicate within the lab.


## Step 4. Import Kali Linux

The Kali Linux virtual machine was downloaded from the official Kali Linux website and imported into VirtualBox.

The VM network adapter was configured as follows:

```text
Adapter 1
Attached to: NAT Network
Network:     NatNetwork
Adapter Type: Intel PRO/1000 MT Desktop
```

The VM was allocated:

```text
RAM: 4096 MB
```
<img width="900" height="553" alt="image" src="https://github.com/user-attachments/assets/c412fbf9-709f-4ce2-b653-2a8eb144f3d3" />

A shared folder was also configured for transferring required files between the host operating system and the Kali VM.



---

## Step 5. Configure the Kali Linux Network

The Kali Linux network configuration was checked and configured with a consistent IPv4 address.

Example configuration:

```text
IP Address: 10.0.0.2
Subnet Mask: 255.255.255.0
Gateway: 10.0.0.1
DNS: 8.8.8.8
```

A consistent IP address makes it easier to document the lab and reference the Kali machine in future exercises.

![](4-screenshot-kali-network-settings.png)

---

## Step 6. Create a Clean VM Snapshot

After completing the initial configuration, a VirtualBox snapshot was created.

Example snapshot name:
<img width="1360" height="768" alt="image" src="https://github.com/user-attachments/assets/1b6a5472-d967-4fe5-b54b-cd0bb03aaab9" />


The snapshot represents the clean baseline of the laboratory.

If a future exercise changes or damages the VM configuration, the machine can be restored to this baseline.

## ⚙️ Setup Steps

1. Install Oracle VirtualBox.
2. Download and import Kali Linux.
3. Create a NAT Network in VirtualBox.
4. Connect the Kali Linux VM to the virtual network.
5. Configure and verify the IP address.
6. Test network connectivity and DNS resolution.
7. Create a clean virtual machine snapshot.

## 🔎 Network Verification

Check the IP address:

```bash
ip addr
```

Check the routing table:

```bash
ip route
```

Test connectivity to the gateway:

```bash
ping -c 4 10.0.0.1
```

Test internet connectivity:

```bash
ping -c 4 8.8.8.8
```

Check DNS resolution:

```bash
nslookup networkwalks.com
```

Verify Nmap:

```bash
nmap --version
```

*The IP addresses above are examples. Replace them with the addresses configured in your own lab.*

## KALI LINUX CONFIGURE


<img width="1347" height="604" alt="image" src="https://github.com/user-attachments/assets/bca4b326-d8b6-4d74-a6c2-1b67afb33d1f" />




```

## 📚 Learning Outcomes

- Understanding virtual machine networking.
- Configuring IPv4 addresses and DNS.
- Testing network connectivity.
- Using basic Linux networking commands.
- Creating VM snapshots for recovery.
- Documenting a cybersecurity lab.

## 🔐 Ethical Use

This lab is intended for educational purposes and authorized security testing. Only test systems you own or have explicit permission to assess.

## 🔗 Resources

- [Kali Linux](https://www.kali.org/get-kali/)
- [Oracle VirtualBox](https://www.virtualbox.org/wiki/Downloads)
- [Nmap](https://nmap.org/)

## 👤 Author

**Abhishek Jain**

BCA Student | Cybersecurity Learner
