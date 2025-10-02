# CYBERSECURITY-APEX-TASK-1

# 🛡️ Cybersecurity — Foundation & Environment Setup

This repository documents **Task‑1: Foundation & Environment Setup** — a step‑by‑step record of my cybersecurity learning and lab environment build.

**Goal:** build strong fundamentals in **cybersecurity, networking, and cryptography**, and set up a private Kali‑based hacking lab for safe, legal practice.

---

## 📚 Table of Contents

* [Objectives](#-objectives)
* [What's Included](#-whats-included)
* [Steps Covered](#-steps-covered)
* [Deliverables & Directory Structure](#-deliverables--directory-structure)
* [Quick Verification (How to reproduce)](#-quick-verification-how-to-reproduce)
* [Commands & Examples](#-commands--examples)
* [Key Learnings / Summary](#-key-learnings--summary)
* [Checklist for Submission](#-checklist-for-submission)
* [Safety & Responsible Use](#-safety--responsible-use)
* [How I Submitted This Task](#-how-i-submitted-this-task)
* [Screenshots & Video](#-screenshots--video)
* [License](#-license)

---

## 📌 Objectives

* Build strong fundamentals in **cybersecurity and networking**.
* Gain hands‑on experience with a private Kali Linux attacker VM and intentionally vulnerable targets (DVWA / Metasploitable2).
* Become familiar with basic **Linux**, **cryptography**, and essential tools (Nmap, Wireshark, Burp Suite).
* Learn safe, responsible lab practices for ethical security learning.

---

## ⚡ Steps Covered

1. **Cybersecurity Basics** — CIA Triad, threat types, common attack vectors.
2. **Lab Environment Setup** — VirtualBox setup, Kali (attacker), Metasploitable2 / DVWA (targets), Host‑Only networking.
3. **Linux Fundamentals** — shell navigation, file permissions, package management, basic networking commands.
4. **Networking** — OSI/TCP‑IP model, DNS, HTTP/HTTPS, IP addressing & subnetting.
5. **Cryptography** — symmetric vs asymmetric cryptography, hashing, SSL/TLS basics, OpenSSL examples.
6. **Tools** — practical hands‑on with Wireshark, Nmap, Burp Suite, Netcat, and Tshark.

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
├─ Burpsuite Execution.png
├─ Kali Linux Setup.jpg
├─ Kali Linux Nmap Result.jpg
├─ Metasploitable 2 Setup.png
├─ Oracle VirtualBox Setup.png
└─ Wireshark Ping Execution.jpg
VIDEO/
└─ lab_setup_walkthrough.mp4
README.md
LICENSE
```
---

## ✅ Quick Verification (How to reproduce)

> Host‑only subnet example used for the lab: `192.168.56.0/24`

**Example static IP plan**

* Host (VBox host‑only): `192.168.56.1`
* Kali (attacker): `192.168.56.101`
* Metasploitable (target): `192.168.56.102`

**Basic verification commands (run on Kali)**

```bash
# show interface and IP
ip a

# ping the target
ping -c 4 192.168.56.102

# basic TCP SYN nmap scan (requires sudo)
sudo nmap -sS -Pn 192.168.56.102

# capture a small packet trace (tshark) - CLI
sudo tshark -i eth0 -c 50 -w /tmp/capture.pcap
```

---

## 🧰 Commands & Examples (short cheatsheet)

* `sudo apt update && sudo apt upgrade -y` — update Kali packages.
* `sudo apt install nmap wireshark tshark -y` — install common tools.
* `nmap -sS -Pn <target-ip>` — stealth SYN scan (use responsibly).
* `tshark -i eth0 -c 100 -w capture.pcap` — capture 100 packets to a pcap file.
* `curl -I http://<target-ip>` — check HTTP headers.

---

## 📝 Key Learnings / Summary

* Gained hands‑on experience setting up a contained penetration‑testing lab using VirtualBox host‑only networking.
* Practiced network discovery and basic service enumeration with Nmap.
* Collected and analyzed packet captures with Tshark/Wireshark to understand network behavior.
* Reviewed fundamental cryptography concepts and practiced with OpenSSL for basic certificate and hashing exercises.
* Reinforced the importance of responsible and ethical practices when experimenting with security tools.

---

## 📝 Checklist for Submission

* [ ] `Lab_Setup_Report.md` with inline screenshots.
* [ ] `CHEAT_SHEETS/Linux_CLI_CheatSheet.md` added.
* [ ] `CHEAT_SHEETS/Tool_Commands_CheatSheet.md` added.
* [ ] `SCREENSHOTS/` contains the listed images with correct filenames.
* [ ] `VIDEO/lab_setup_walkthrough.mp4` recorded and uploaded.
* [ ] README includes verification steps and IP plan.
* [ ] Linked video added to LinkedIn Featured and link included in ApexPlanet submission.
* [ ] Public GitHub repo link copied to ApexPlanet task entry.

---

## ⚠️ Safety & Responsible Use

This lab is for **educational, legal, and ethical** use only.

* **Do not** run attacks, scans, or exploit code against systems you do not own or do not have explicit permission to test.
* **Isolate your lab**: keep the attacker and target VMs in a host‑only or NAT network that is not bridged to your production or home network.
* Avoid connecting intentionally vulnerable VMs to the Internet.
* Keep snapshots of your VMs before major changes so you can quickly restore a clean state.

---

## 📤 How I Submitted This Task

1. Recorded a walkthrough: `VIDEO/lab_setup_walkthrough.mp4`.
2. Uploaded the walkthrough video to LinkedIn (Added it under *Featured*).
3. Pushed all files to this public GitHub repo.
4. Logged into ApexPlanet → Manage Task → pasted LinkedIn video link & GitHub repo link → submitted.

---

## 🖼️ Screenshots & Video

All screenshots used in the `Lab_Setup_Report.md` (filenames as committed):

* `SCREENSHOTS/Burpsuite Execution.png`
* `SCREENSHOTS/Kali Linux Setup.jpg`
* `SCREENSHOTS/Kali Linux Nmap Result.jpg`
* `SCREENSHOTS/Metasploitable 2 Setup.png`
* `SCREENSHOTS/Oracle VirtualBox Setup.png`
* `SCREENSHOTS/Wireshark Ping Execution.jpg`

**Video (LinkedIn)**

* LinkedIn walkthrough: [https://www.linkedin.com/posts/nikhat-naaz-malki-shaik-8240aa31a_cybersecurity-internship-ethicalhacking-activity-7379474614701228033-ja0Z](https://www.linkedin.com/posts/nikhat-naaz-malki-shaik-8240aa31a_cybersecurity-internship-ethicalhacking-activity-7379474614701228033-ja0Z)

---

## 📄 License

This project is licensed under the MIT License — see the `LICENSE` file for details.

---

