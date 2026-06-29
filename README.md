# Network Security Lab

A practical network security project focused on securing communications,
configuring firewalls, and analyzing network traffic in a virtualized environment.

---

## Project Overview
This project simulates a real-world secure network setup using three Ubuntu
machines connected in a private network via VirtualBox. It covers the full
cycle of network security: configuration, hardening, and monitoring.

---

## Environment Setup
| Machine | IP Address |
|---|---|
| Ubuntu Base | 192.168.56.101 |
| Ubuntu-1 | 192.168.56.102 |
| Ubuntu-2 | 192.168.56.103 |

---

## Task 1: Network Configuration, SSH & File Transfer
- Verified network interfaces on all machines using `ip addr`
- Established SSH connections between all three machines
- Created files remotely via SSH
- Transferred files securely between machines using `scp`
- Restarted and verified SSH service status using `systemctl`

---

## Task 2: Firewall Configuration (UFW)
- Installed and configured UFW on all machines
- Allowed SSH traffic (port 22) through the firewall
- Enabled firewall on system startup
- Verified firewall rules using `sudo ufw status`
- Confirmed SSH connectivity remains active after firewall enforcement
- Verified ICMP (ping) traffic between all machines

---

## Task 3: Network Traffic Monitoring (Wireshark)
Captured and analyzed three types of network traffic:

**SSH Traffic**
- Observed SSHv2 key exchange (New Keys)
- Confirmed all data transmitted as encrypted packets

**ICMP Traffic (Ping)**
- Captured Echo Request and Echo Reply packets
- Confirmed 0% packet loss across all machines

**TCP Traffic (SCP File Transfer)**
- Observed TCP three-way handshake (SYN → SYN/ACK → ACK)
- Confirmed file transfer encrypted over port 22 via SSHv2

---

## Tools & Technologies
- VirtualBox
- Ubuntu 24.04 LTS
- SSH / SCP
- UFW (Uncomplicated Firewall)
- Wireshark
- Linux CLI
