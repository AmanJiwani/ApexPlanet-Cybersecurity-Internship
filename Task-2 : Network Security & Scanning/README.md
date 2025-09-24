# 🛡️ Network Scanning & Vulnerability Assessment Project

![License](https://img.shields.io/badge/License-MIT-blue)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)

---

## 👤 Author
**Aman Jiwani**  

---

## 🎯 Objective
Demonstrate fundamental cybersecurity operations in a lab environment, including:

- Reconnaissance (Passive & Active)  
- Port & Service Scanning  
- Vulnerability Assessment  
- Packet Analysis  
- Firewall Configuration  

---

## 💻 Lab Setup
| Component        | Details           |
|-----------------|-----------------|
| Attacker VM      | Kali Linux       |
| Target VM        | Metasploitable2  |
| Network          | Host-only        |

---

## 🗂️ Tasks & Methodology

### 1️⃣ Reconnaissance
- **Passive Recon:** Whois, Nslookup, Google Dorking, Shodan  
- **Active Recon:** Ping Sweep, Banner Grabbing  

### 2️⃣ Port & Service Scanning
- Nmap TCP & UDP Scans  
- Service Version Detection (`-sV`)  
- OS Detection (`-O`)  
- Scan report included in [`/nmap/nmap_scan_report.md`](./nmap/nmap_scan_report.md)

### 3️⃣ Vulnerability Scanning
- Nessus Essentials used for scanning  
- Scan report and analysis in [`/vuln_scanning/`](./vuln_scanning/)

### 4️⃣ Packet Analysis
- Captured HTTP, FTP, DNS traffic  
- Filtered credentials from unencrypted FTP  
- Simulated SYN flood attack using `hping3`  
- Packet captures stored in [`/packet_analysis/`](./packet_analysis/)

### 5️⃣ Firewall Basics
- Configured `iptables` rules to allow/deny specific ports  
- Demonstrated blocking a port scan attempt  
- Files stored in [`/firewall/`](./firewall/)

---

## 📦 Deliverables
- Nmap Scan Report  
- Nessus/OpenVAS Vulnerability Report  
- Packet captures (`.pcap`)  
- Firewall rules and demonstration  
- [Demo Video Link](demo_video_link.txt)

---

## 📊 Observations & Learning
- Identified open ports and running services on the target  
- Detected vulnerabilities and classified by severity (Critical/High/Medium/Low)  
- Extracted sensitive data from unencrypted traffic (FTP, HTTP)  
- Tested firewall rules to block unauthorized access and port scans  
- Learned practical application of scanning and monitoring techniques in a lab environment  

---

## ⚡ Notes
- All experiments conducted in a safe, isolated host-only lab environment  
- No sensitive or personal data exposed  
- Workflow designed to demonstrate SOC-level reconnaissance and scanning skills  


