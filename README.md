# Task 1  Basic Network Scanning with Nmap

**Intern:** Mohammed Altaf Hussain  
**Internship:** AICTE Oasis Infobyte - Security Analyst Intern  
**Task:** Basic Network Scanning with Nmap  
**Target:** TARGET

## Command used
sudo nmap -sS -sV -O -p- -T4 --min-rate=300 -oN nmap_scan_results.txt TARGET

## Findings (summary)
- Open ports found: 135, 139, 445, 808, 912, 2179, 2869, 3306, 5040, 5357, 33060, 49664â,49668, 49674, 51557
- Services and versions:
  - 135: Microsoft Windows RPC
  - 139: Microsoft Windows netbios-ssn
  - 445: microsoft-ds?
  - 3306: MySQL (unauthorized)
  - 5357: Microsoft HTTPAPI httpd 2.0
  - 912: VMware Authentication Daemon
- OS Detection: Likely Windows XP SP3, Windows 7, or Windows Server 2012 (98% confidence)

## Significance of open ports
- **135/139/445 (RPC/NetBIOS/SMB)**  Common Windows services; can be vulnerable if exposed.
- **3306/33060 (MySQL)**  Database ports; should be secured or firewalled.
- **5357/2869 (HTTPAPI)**  Web services; may expose system info.
- **912 (VMware)**  Indicates virtualization; may expose remote access.
- **51557 (tcpwrapped)** Service protected by a wrapper or firewall.

## Conclusion and recommendations
The host exposes several Windows services and a MySQL database. These should be reviewed for unnecessary exposure, patched, and protected with firewalls and strong credentials
