# Tool Commands Cheat Sheet — Task 6 (Nmap, Netcat, Wireshark, Burp)


| Tool   | Command            | Purpose                                                        | Example                   |
|--------|--------------------|----------------------------------------------------------------|---------------------------|
| Nmap   | `nmap [IP]`        | Basic scan: checks ≈1000 common TCP ports.                     | `nmap 192.168.56.101`     |
| Nmap   | `nmap -sV [IP]`    | Service version detection on open ports.                       | `nmap -sV 192.168.56.101` |
| Nmap   | `nmap -A [IP]`     | Aggressive scan: OS detection, version detection, scripts, traceroute. | `nmap -A 192.168.56.101`  |
| Ping   | `ping [IP]`        | Network connectivity test (sends ICMP packets).                | `ping 192.168.56.101`     |
| Netcat | `nc -lvp [PORT]`   | Listener: opens a TCP port and waits for incoming connections. | `nc -lvp 4444`            |

