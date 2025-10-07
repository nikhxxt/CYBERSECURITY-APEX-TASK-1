# CYBERSECURITY-APEX-TASK-1 ⚡️

## 🛡️ Cybersecurity — Foundation & Environment Setup

**Task‑1:** Step-by-step documentation of setting up a contained cybersecurity lab (Kali Linux attacker VM + vulnerable targets) to learn networking, enumeration, packet capture, and basic cryptography.

**Goal:** Build practical skills with VirtualBox, Kali Linux, Metasploitable2/DVWA, and tools like `nmap`, `Wireshark`, `Burp Suite`. Includes reproducible steps, labeled screenshots, and a short walkthrough video.

---

## 🔖 Badges
[![License: MIT](https://img.shields.io/badge/License-MIT-green)](LICENSE)
![Repo size](https://img.shields.io/github/repo-size/nikhxxt/CYBERSECURITY-APEX-TASK-1)
![GitHub stars](https://img.shields.io/github/stars/nikhxxt/CYBERSECURITY-APEX-TASK-1?style=social)
![GitHub forks](https://img.shields.io/github/forks/nikhxxt/CYBERSECURITY-APEX-TASK-1?style=social)

---

## 📚 Table of Contents

* [What’s Included](#whats-included)
* [Quick Start — Reproduce the Lab](#quick-start---reproduce-the-lab)
* [Folder Structure](#folder-structure)
* [Commands & Verification Snippets](#commands--verification-snippets)
* [Screenshots & Video References](#screenshots--video-references)
* [Checklist Before Submission](#checklist-before-submission)
* [Notes & Recommended Improvements](#notes--recommended-improvements)
* [License & Contact](#license--contact)

---

## 📦 What’s Included

### CHEAT_SHEETS

* `Linux_CLI_CheatSheet.md`
* `Tool_Commands_CheatSheet.md`

### FOUNDATION

* `Lab_Setup_and_Verification.md`
* `Task3_Networking_Notes.md`
* `Task4_Cryptography_Notes.md`

### SCREENSHOTS

* `Burpsuite Exceution.png` 
* `Kali Linux Setup.jpg`
* `Kali Linux nmap Result.jpg`
* `Metasploitable 2 Setup.png`
* `Oracle VirtualBox Setup.png`
* `Wireshark Ping Execution.jpg`

### VIDEO

* `lab_setup_walkthrough.mp4` 

### LICENSE

* MIT License included

---

## Quick Start — Reproduce the Lab

1. **Clone the repository**

```bash
git clone https://github.com/nikhxxt/CYBERSECURITY-APEX-TASK-1.git
cd CYBERSECURITY-APEX-TASK-1
```

2. **Download required images**

* Kali Linux ISO
* Metasploitable2 OVA

3. **Create VirtualBox VMs**

* Host‑Only network: `192.168.56.0/24`
* Import Metasploitable2 OVA
* Create Kali VM with ISO attached

4. **Start VMs and verify connectivity**

```bash
# On Kali
ip a
ping -c 3 192.168.56.102   # replace with target IP

# Quick nmap scan
sudo nmap -sS -Pn 192.168.56.102
```

---

## Commands & Verification Snippets

### System Update & Tool Installation

```bash
sudo apt update && sudo apt upgrade -y
sudo apt install -y nmap wireshark tshark burpsuite
```

### Networking Verification

```bash
ip a        # check interfaces and IPs
ip route    # routing table
ping -c 4 192.168.56.102  # test connectivity (replace with your target IP)
```

### Nmap Scans

```bash
# Top 100 ports
nmap -T4 --top-ports 100 192.168.56.102

# Full port scan with service/version detection
sudo nmap -sS -sV -p- 192.168.56.102
```

### Packet Capture with Tshark

```bash
# Replace `eth0` with your Kali VM's network interface (use `ip a` to find the correct name)
sudo tshark -i eth0 -c 100 -w /tmp/capture.pcap
```

### Notes on interfaces & permissions

* Network interface names may vary (common examples: `eth0`, `ens33`, `enp0s3`, `eth1`). Run `ip a` to find the correct interface.
* For Wireshark/tshark packet captures you may need root privileges or to add your user to the `wireshark` group:

```bash
# run Wireshark as root (not recommended for long-term use)
sudo wireshark

# OR (recommended) add user to wireshark group and re-login
sudo usermod -aG wireshark $USER
```

* If `tshark` or `wireshark` cannot see interfaces, check VirtualBox network settings (Host‑Only adapter vs NAT) and ensure VMs are on the same subnet.


---

## Screenshots & Video References

| Screenshot                   | Description                  |
| ---------------------------- | ---------------------------- |
| Oracle VirtualBox Setup.png  | VM creation & network setup  |
| Kali Linux Setup.jpg         | Kali installation screenshot |
| Metasploitable 2 Setup.png   | Target VM boot & login       |
| Kali Linux nmap Result.jpg   | Sample nmap scan results     |
| Wireshark Ping Execution.jpg | ICMP capture example         |
| Burpsuite Exceution.png      | Burp Suite intercept demo    |

**LinkedIn walkthrough:** (https://www.linkedin.com/posts/nikhat-naaz-malki-shaik-8240aa31a_cybersecurity-internship-ethicalhacking-activity-7379474614701228033-ja0Z?utm_source=share&utm_medium=member_desktop&rcm=ACoAAFDQ0hwBssVRSllABDcGpxoifixeymEi_nY)

---

## Checklist Before Submission

* [ ] `Lab_Setup_and_Verification.md` includes all commands & expected outputs
* [ ] Screenshots are present & referenced
* [ ] Cheat sheets contain copyable commands
* [ ] Walkthrough video uploaded to LinkedIn Featured
* [ ] MIT License included
* [ ] README includes TOC, commands, and verification steps

---

## License & Contact

This project is licensed under the **MIT License** — see `LICENSE`.
Repo: [https://github.com/nikhxxt/CYBERSECURITY-APEX-TASK-1](https://github.com/nikhxxt/CYBERSECURITY-APEX-TASK-1)

