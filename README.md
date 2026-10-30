# 🔐 Cybersecurity Lab Setup

## 📌 Overview
This project involves setting up a virtual cybersecurity lab using Kali Linux and Oracle VirtualBox. The lab provides an environment for learning network configuration, reconnaissance, and ethical hacking techniques.

## 🎯 Objectives
- Install Kali Linux in VirtualBox.
- Configure virtual networking.
- Understand IP addressing and network connectivity.
- Test internet and DNS connectivity.
- Create a virtual machine snapshot.
- Prepare a lab for cybersecurity practice.

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

## 📸 Screenshots

Add screenshots of your actual configuration and test results.

Suggested folder structure:

```text
cybersecurity-lab/
├── README.md
└── screenshots/
    ├── virtualbox-network.png
    ├── kali-desktop.png
    ├── ip-configuration.png
    └── connectivity-test.png
```

Display a screenshot in your README using:

```markdown
![Kali Linux Network Configuration](screenshots/ip-configuration.png)
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
