

# CYBERSECURITY-APEX-TASK-1
# 🛡️ Cybersecurity Foundation & Environment Setup

This repository documents **Task‑1: Foundation & Environment Setup** — a step-by-step record of my cybersecurity learning and lab environment build.  
Goal: build strong fundamentals in **cybersecurity, networking, cryptography**, and set up a private Kali‑based hacking lab for safe practice.

---

## 📚 Table of Contents
- [Objectives](#-objectives)  
- [Steps Covered](#-steps-covered)  
- [Deliverables & Directory Structure](#-deliverables--directory-structure)  
- [Quick Verification (How to reproduce)](#-quick-verification-how-to-reproduce)  
- [Checklist for Submission](#-checklist-for-submission)  
- [Safety & Responsible Use](#-safety--responsible-use)  
- [How I Submitted This Task](#-how-i-submitted-this-task)  
- [Contact & License](#-contact--license)

---

## 📌 Objectives
- Build fundamentals in **Cybersecurity & Networking**  
- Learn: **CIA Triad, Threats, Attack Vectors**  
- Set up a **Kali Linux** attacker VM, and vulnerable targets (DVWA / Metasploitable2)  
- Become familiar with basic **Linux**, **cryptography**, and essential tools (Nmap, Wireshark, Burp)

---

## ⚡ Steps Covered
1. **Cybersecurity Basics** — CIA Triad, Threat Types, Attack Vectors  
2. **Lab Environment Setup** — VirtualBox, Kali (attacker), Metasploitable2 / DVWA (targets), Host‑Only network  
3. **Linux Fundamentals** — navigation, permissions, packages, networking commands  
4. **Networking** — OSI/TCP‑IP, DNS, HTTP/HTTPS, IP addressing & subnetting  
5. **Cryptography** — symmetric/asymmetric, hashing, SSL/TLS, OpenSSL examples  
6. **Tools** — Wireshark, Nmap, Burp Suite, Netcat

---

## 🔧 Deliverables & Directory Structure
```

FOUNDATION/
├─ Lab_Setup_Report.md
├─ Task3_Networking_Notes.md
└─ Task4_Cryptography_Notes.md
CHEAT_SHEETS/
├─ Linux_CLI_CheatSheet.md
└─ Tool_Commands_CheatSheet.md
SCREENSHOTS/
├─ Oracle VirtualBox Setup.png
├─ Kali Linux Setup.jpg
├─ Metasploitable 2 Setup.png
├─ Kali Linux nmap Result.jpg
└─ Wireshark Ping Execution.jpg
VIDEO/
└─ lab_setup_walkthrough.mp4
README.md

````

**Key files**
- `FOUNDATION/Lab_Setup_Report.md` — step‑by‑step setup with commands and screenshots.  
- `CHEAT_SHEETS/Linux_CLI_CheatSheet.md` — quick CLI reference.  
- `CHEAT_SHEETS/Tool_Commands_CheatSheet.md` — Nmap/Netcat/Wireshark/Burp commands.  
- `SCREENSHOTS/` and `VIDEO/` — visual evidence used for submission.

---

## ✅ Quick Verification (How to reproduce)
> Use the Host‑Only network `192.168.56.0/24` (example). Replace IPs if you chose different ones.

**Example static IP plan**
- Host (VBox host-only): `192.168.56.1`  
- Kali (attacker): `192.168.56.101`  
- Metasploitable (target): `192.168.56.102`

**Commands to verify (run on Kali)**
```bash
# show interface and IP
ip a

# ping target
ping -c 4 192.168.56.102

# basic nmap scan
sudo nmap -sS -Pn 192.168.56.102

# capture a small packet trace (tshark) - CLI
sudo tshark -i eth0 -c 50 -w /tmp/capture.pcap
````

**Expected results**

* `ping` replies from `192.168.56.102`.
* `nmap` shows open services on the target (e.g., ports 22, 80, 445 etc. depending on the target image).
* `capture.pcap` contains ICMP and TCP frames that can be opened in Wireshark.

---

## 📝 Checklist for Submission

* [ ] `Lab_Setup_Report.md` with inline screenshots.
* [ ] `CHEAT_SHEETS/Linux_CLI_CheatSheet.md` added.
* [ ] `CHEAT_SHEETS/Tool_Commands_CheatSheet.md` added.
* [ ] `SCREENSHOTS/` contains the listed images.
* [ ] `VIDEO/lab_setup_walkthrough.mp4` recorded and uploaded.
* [ ] README includes verification steps and IP plan.
* [ ] Linked video added to LinkedIn Featured and link included in ApexPlanet submission.
* [ ] Public GitHub repo link copied to ApexPlanet task entry.

---

## ⚠️ Safety & Responsible Use

This lab is for **educational, legal, and ethical** use only.
**Do not** run attacks or scans against systems you do not own or have explicit permission to test. Use only your private VM lab or sanctioned targets.



## 📤 How I Submitted This Task

1. Recorded a 5‑minute walkthrough: `VIDEO/lab_setup_walkthrough.mp4`.
2. Uploaded video to LinkedIn (added under *Featured*) and copied the share link.
3. Pushed all files to this public GitHub repo.
4. Logged in to ApexPlanet → Manage Task → pasted LinkedIn video link & GitHub repo link → submitted.



