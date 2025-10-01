# Task 3 — Networking Notes


## 1. Why networking matters in cybersecurity
Understanding networks is essential for reconnaissance, exploitation, traffic analysis, and defending infrastructure. Attackers and defenders both need to read network behavior.


## 2. OSI Model (7 layers) — short summary
1. **Physical (Layer 1)** — cables, NICs, electrical signals.
2. **Data Link (Layer 2)** — MAC addresses, switches, Ethernet frames.
3. **Network (Layer 3)** — IP addressing, routing (IPv4/IPv6).
4. **Transport (Layer 4)** — TCP/UDP, ports, segmentation, reliable vs unreliable transport.
5. **Session (Layer 5)** — session management (less prominent in TCP/IP shorthand).
6. **Presentation (Layer 6)** — data representation, encryption/encoding.
7. **Application (Layer 7)** — HTTP, FTP, SSH, DNS — protocols apps use.


> Common mapping: OSI layers 5-7 often represented by the Application layer in the TCP/IP model.


## 3. TCP/IP Model (concise)
- **Link** (Network Interface) — Ethernet, ARP
- **Internet** — IP (routing)
- **Transport** — TCP, UDP
- **Application** — HTTP, DNS, SMTP, etc.


## 4. IPv4 addressing & subnetting (practical)
- IPv4 address format: `A.B.C.D` (32 bits). Example: `192.168.56.20`.
- CIDR notation: `192.168.56.0/24` means netmask `255.255.255.0` (24 bits network). Hosts: 2^(32-24)-2 = 254 usable.


### Quick subnetting examples
- `/24` → 256 addresses → 254 hosts per subnet.
- `/28` → 16 addresses → 14 hosts per subnet.
- To get network & broadcast:
- Network = set host bits to 0. Broadcast = set host bits to 1.


### Calculating subnets (short method)
- Borrowed bits = (new mask - old mask). Hosts = 2^(host bits) - 2.


## 5. Common protocols to know
- **ARP** — resolves IPv4 to MAC (Layer 2). `arp -a` to view ARP table.
- **ICMP** — ping (echo request/reply), useful for host discovery.
- **TCP** — 3-way handshake (SYN, SYN-ACK, ACK), connection-oriented.
- **UDP** — connectionless, used by DNS, DHCP, etc.


## 6. Ports and services
- Well-known ports: 21 (FTP), 22 (SSH), 23 (Telnet), 25 (SMTP), 53 (DNS), 80 (HTTP), 443 (HTTPS), 3306 (MySQL), 445 (SMB).
- Use `ss -tuln` or `netstat -tuln` to list listening ports.


## 7. Practical commands (quick)
show IP addresses - ip a
show routing table - ip route show
ARP cache - arp -n
list listening sockets - ss -tuln
ping a host - ping -c 4 192.168.56.20
