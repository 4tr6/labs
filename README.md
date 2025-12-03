# Network Reconnaissance Lab Report

This is an internal cybersecurity training lab reconnaissance scan using Linux commands and Nmap in a controlled environment.

---

## 1) Network Range Discovery
Command used:  
`ip route`

Result:  
192.168.243.0/24

---

## 2) Live Hosts Discovery
Command used:  
`nmap -sn 192.168.243.0/24`

Result:  
5 hosts are up, including the target: 192.168.243.134

---

## 3) Service Enumeration (Indirect OS Detection)
Command used:  
`sudo nmap -sV 192.168.243.134`

Result:  
- 21/tcp → FTP → vsftpd 2.3.4 (old & vulnerable)  
- 22/tcp → SSH → OpenSSH 4.7p1 Debian (outdated)  
- 23/tcp → Telnet → Linux telnetd (unsafe, plaintext protocol)

---

## Notes
These services are intentionally outdated because this is a training environment for learning attack surface enumeration and exploit research.

---

## Disclaimer
This is a personal training lab scan. No external or unauthorized systems were targeted.
