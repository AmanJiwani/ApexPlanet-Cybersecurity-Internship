# Networking Basics  

This document covers the core concepts of networking: **OSI Model, TCP/IP Model, DNS, and IP Addressing**.  

---

## 🌐 1. OSI Model (Open Systems Interconnection)  

The OSI model is a **conceptual framework** that standardizes the functions of a networking system into 7 layers.  

| Layer | Name              | Function                                                                 | Example Protocols |
|-------|-------------------|--------------------------------------------------------------------------|-------------------|
| 7     | **Application**   | Interface for user applications to access network services               | HTTP, FTP, SMTP   |
| 6     | **Presentation**  | Data translation, encryption, compression                                | SSL/TLS, JPEG     |
| 5     | **Session**       | Establish, manage, and terminate communication sessions                  | NetBIOS, PPTP     |
| 4     | **Transport**     | Ensures reliable delivery (error checking, flow control, segmentation)   | TCP, UDP          |
| 3     | **Network**       | Logical addressing, routing                                              | IP, ICMP, ARP     |
| 2     | **Data Link**     | Physical addressing (MAC), error detection                              | Ethernet, PPP     |
| 1     | **Physical**      | Transmission of raw bits over a medium                                   | Cables, Wi-Fi     |

👉 **Tip to remember**: *All People Seem To Need Data Processing* (Application → Physical).  

---

## 🌍 2. TCP/IP Model  

The **TCP/IP model** is more practical and widely used in real-world networks. It has **4 layers**.  

| Layer | Equivalent OSI Layer(s)     | Function                                   | Example Protocols |
|-------|-----------------------------|--------------------------------------------|-------------------|
| 4     | Application (7–5)           | End-user services and protocols            | HTTP, DNS, FTP    |
| 3     | Transport (4)               | Reliable/unreliable delivery, ports        | TCP, UDP          |
| 2     | Internet (3)                | Logical addressing and routing             | IP, ICMP, ARP     |
| 1     | Network Access (2–1)        | Physical addressing and media access       | Ethernet, Wi-Fi   |

👉 **Difference from OSI**: OSI has **7 layers**, TCP/IP has **4 layers**. TCP/IP is used in practice, OSI is theoretical.  

---

## 🌐 3. DNS (Domain Name System)  

DNS is the **phonebook of the internet**. It translates **human-readable domain names** (e.g., `google.com`) into **IP addresses** (e.g., `142.250.183.206`).  

### 🔑 Key Components:  
- **Domain Name** → `example.com`  
- **DNS Resolver** → Sends queries on behalf of the client  
- **Root Servers** → Store root domain info (.)  
- **TLD Servers** → Handle extensions like `.com`, `.org`, `.in`  
- **Authoritative Servers** → Store the actual domain records  

### 📄 Types of DNS Records:  
- **A Record** → Maps a domain to IPv4 address  
- **AAAA Record** → Maps a domain to IPv6 address  
- **CNAME Record** → Alias for another domain  
- **MX Record** → Mail server  
- **TXT Record** → Text info (e.g., SPF, DKIM for email security)  

👉 Example:  
```bash
nslookup google.com
