# 🚀 ApexPlanet Cybersecurity & Ethical Hacking Internship

**Internship Duration:** 01 Sept 2025 – 30 Oct 2025  
**Intern:** Aman Jiwani  
**Internship ID:** APSPL2518053

Welcome to my GitHub repository showcasing all tasks, projects, and deliverables completed during my **Cybersecurity & Ethical Hacking Internship** at ApexPlanet Software Pvt. Ltd.  

All work was performed in a controlled lab environment using Kali Linux (attacker) and Metasploitable2 (target) in host-only network configuration.  

---

## 📚 Completed Tasks

### ✅ Task 1 – Foundations of Cybersecurity
- **Fundamentals Learned:** CIA Triad, Threat types, Attack vectors  
- **Lab Setup:** Kali Linux & Metasploitable2  
- **Linux & Networking:** File navigation, permissions, package management, `ip/ifconfig`, `ping`, `traceroute`  
- **Cryptography Basics:** Symmetric/asymmetric encryption, hashing, SSL/TLS  
- **Tool Familiarization:** Wireshark, Nmap, Burp Suite  

**Deliverables (Task 1)**  
- Lab Setup Report with screenshots  
- Linux Command Notes & Cheat Sheet  
- Initial tool testing outputs (Wireshark, Nmap)  
- 5-minute demo video of lab setup and basic scans  

**Key Learnings (Task 1)**  
- Built a safe, isolated hacking lab  
- Understood basic offensive/defensive concepts and common tools  
- Practiced Linux & basic networking operations  
- Explored cryptography basics (encryption, hashing, SSL/TLS)  
- Gained familiarity with Wireshark, Nmap, and Burp Suite  

---

### ✅ Task 2 – Network Scanning & Vulnerability Assessment
**Objective:** Perform reconnaissance, scanning, vulnerability assessment, packet analysis, and firewall demonstration on the target VM (Metasploitable2).

#### Steps & Tasks
1. **Reconnaissance**
   - Passive: `whois`, `nslookup`, Google dorking notes, Shodan (lab-only)  
   - Active: Ping sweep, banner grabbing using `telnet` / `netcat`  

2. **Port & Service Scanning (Nmap)**
   - **Full TCP Port Scan:** `sudo nmap -Pn -p- -T4 <TARGET_IP>`  
   - **SYN Stealth + Service Version + OS Detection:** `sudo nmap -sS -sV -O --osscan-guess -p- -T4 <TARGET_IP>`  
   - **UDP Scan (Targeted):** `sudo nmap -sU -p 53,67,68,69,123,161 -T3 <TARGET_IP>`  
   - Notes on open ports, services, OS info, and risky ports (FTP 21, SSH 22, Telnet 23)  
   - Commands documented in `/nmap/scan_commands.md`  
   - Observations summarized in `/nmap/nmap_scan_report.md`  

3. **Vulnerability Scanning (Nessus Essentials)**
   - Created a basic network scan on target IP  
   - Generated PDF report: `/vuln_scanning/nessus_report.pdf`  
   - Categorized vulnerabilities (Critical, High, Medium, Low)  
   - Remediation suggestions included in `/vuln_scanning/vuln_analysis.md`  

4. **Packet Analysis (Wireshark)**
   - Captured HTTP, FTP, and DNS traffic  
   - Filtered FTP credentials using `frame contains "USER"` and `frame contains "PASS"`  
   - Observed unencrypted protocols leaking sensitive information  
   - Screenshots of captured packets stored in `/packet_analysis/screenshots/`  
   - Notes documented in `/packet_analysis/packet_analysis.md`  

5. **Firewall Basics (iptables)**
   - Cleared old rules and created simple allow/deny rules  
   - Allowed SSH, allowed local loopback, allowed established traffic  
   - Blocked attacker IP (`sudo iptables -A INPUT -s <KALI_IP> -j DROP`)  
   - Demonstrated port scan blocked from Kali VM  
   - Screenshots stored in `/firewall/screenshots/`  
   - Commands and observations documented in `/firewall/firewall.md`  

---

## 🛠️ Tools & Technologies (Task 2)
- **Operating Systems:** Kali Linux, Metasploitable2  
- **Scanning & Vulnerability Assessment:** Nmap, Nessus Essentials  
- **Packet Analysis:** Wireshark  
- **Firewall:** iptables  
- **Environment:** Host-only virtual lab (isolated, safe)

---
## 📌 Observations & Key Learnings (Task 2)
- **Identified open ports, services, and OS using Nmap 
- **Performed vulnerability assessment and prioritized using CVSS  
- **Captured and analyzed network packets to detect unencrypted credentials
- *Applied firewall rules to block attacker IP and prevent reconnaissance




