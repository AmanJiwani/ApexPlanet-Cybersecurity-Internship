# 🚀 ApexPlanet Cybersecurity & Ethical Hacking Internship

**Internship Duration:** 01 Sept 2025 – 30 Oct 2025  
**Intern:** Aman Jiwani  
**Internship ID:** APSPL2518053

Welcome — this repository contains the tasks, labs, notes and deliverables completed during my **Cybersecurity & Ethical Hacking Internship** at ApexPlanet Software Pvt. Ltd.

---

## 📚 Completed Tasks (Overview)

### ✅ Task 1 – Foundations of Cybersecurity
- **Fundamentals Learned:** CIA Triad, Threat types, Attack vectors  
- **Lab Setup:** Kali Linux (attacker) & Metasploitable2 (target) in host-only network  
- **Linux & Networking:** File navigation, permissions, package management, `ip/ifconfig`, `ping`, `traceroute`  
- **Cryptography Basics:** Symmetric/asymmetric encryption, hashing, SSL/TLS fundamentals  
- **Tool Familiarization:** Wireshark, Nmap, Burp Suite (intro)

**Deliverables (Task 1)**  
- Lab Setup Report with screenshots  
- Linux Command Notes & Cheat Sheet  
- Initial tool testing outputs (Wireshark, Nmap)  
- 5-min video walkthrough (lab demo)

**Key Learnings (Task 1)**  
- Built a safe, isolated hacking lab  
- Understood basic offensive/defensive concepts and common tools  
- Practiced Linux & basic networking operations

---

### ✅ Task 2 – Network Scanning & Vulnerability Assessment (NEW)
**Objective:** Perform full reconnaissance, scanning, vulnerability assessment, packet analysis and a basic firewall demonstration on the lab target (Metasploitable2).

#### Tasks & Steps
1. **Reconnaissance**
   - Passive: `whois`, `nslookup`, Google dorking notes, Shodan results (lab notes)
   - Active: Ping sweep and banner grabbing (telnet/netcat)

2. **Port & Service Scanning**
   - TCP full port sweep and SYN scan (`-sS`, `-p-`)  
   - UDP targeted scans (`-sU`) for DNS/NTP/SNMP etc.  
   - Service version detection (`-sV`) and OS detection (`-O`)  
   - Commands captured and explained in `/nmap/scan_commands.md`

3. **Vulnerability Scanning**
   - Setup & usage of **Nessus Essentials** (or OpenVAS)  
   - Scanned Metasploitable2, exported **Nessus PDF report**  
   - Categorized findings: Critical / High / Medium / Low, with remediation suggestions

4. **Packet Analysis (Wireshark)**
   - Captured and inspected **HTTP, FTP, DNS** traffic  
   - Filtered FTP credentials (unencrypted) using `frame contains "USER"` / `"PASS"`  
   - Saved screenshots of key packets for analysis

5. **Firewall Basics**
   - Created simple `iptables` rules to allow SSH/HTTP and deny rest  
   - Demonstrated blocking a specific attacker IP and showed `nmap` before/after results

#### Tools & Technologies (Task 2)
- **Scanning & Vulnerability:** Nmap, Nessus Essentials (or OpenVAS)  
- **Packet Analysis:** Wireshark  
- **Firewall:** iptables (nft fallback notes if required)  
- **Environment:** Kali Linux (attacker), Metasploitable2 (target), Host-only network

#### Deliverables (Task 2)
- `/nmap/scan_commands.md` — all Nmap commands used (concise, explained)  
- `/nmap/nmap_scan_report.md` — findings, open ports, services, OS detection, recommendations  
- `/vuln_scanning/nessus_report.pdf` — exported Nessus scan (raw)  
- `/vuln_scanning/vuln_analysis.md` — categorized vulnerabilities + remediation steps  
- `/packet_analysis/packet_analysis.md` — Wireshark filters used and observations (screenshots only)  
- `/firewall/firewall.md` — iptables commands used and before/after proof (screenshots)  
- 5-minute demo video (link in `demo_video_link.txt`)

---

## 📁 Recommended Repository Structure
