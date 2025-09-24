Here’s a **short, GitHub-ready Markdown** for your **Firewall Basics lab**, styled like your Nessus and Packet Analysis labs:

````markdown
# Firewall Basics – Metasploitable2 Lab

## Author
Aman Jiwani  

## Date
24 Sep 2025  

## Target
192.168.56.104  

## Attacker (Kali) IP
192.168.56.101  

## Network
Host-only  

---

## Lab Objective
- Create basic firewall rules using iptables.  
- Block a specific attacker IP.  
- Demonstrate filtering of unwanted traffic while allowing essential services.  

---

## Commands on Target (Metasploitable2)

```bash
# 1. Clear old rules
sudo iptables -F
sudo iptables -X

# 2. Allow loopback
sudo iptables -A INPUT -i lo -j ACCEPT

# 3. Allow established connections
sudo iptables -A INPUT -m conntrack --ctstate ESTABLISHED,RELATED -j ACCEPT

# 4. Allow SSH
sudo iptables -A INPUT -p tcp --dport 22 -m conntrack --ctstate NEW -j ACCEPT

# 5. Block attacker IP
sudo iptables -A INPUT -s 192.168.56.101 -j DROP

# 6. Drop all other traffic
sudo iptables -A INPUT -j DROP

# 7. Check rules
sudo iptables -L -v -n --line-numbers
````

**Explanation of Commands**

* `-F / -X` → Clears old rules.
* `-i lo -j ACCEPT` → Allows local programs to communicate.
* `-m conntrack --ctstate ESTABLISHED,RELATED` → Lets return traffic pass.
* `--dport 22 -j ACCEPT` → Allows SSH connections.
* `-s <IP> -j DROP` → Blocks traffic from attacker.
* Final `-j DROP` → Blocks everything else not allowed.

---

## Verification from Attacker (Kali)

**Before firewall:**

```bash
sudo nmap -Pn -sS -p- -T4 <TARGET_IP>
```

**Screenshot:** `screenshots/nmap_before_block.png`

**After firewall rules applied:**

```bash
sudo nmap -Pn -sS -p- -T4 <TARGET_IP>
```

**Screenshot:** `screenshots/nmap_after_block.png`

> Many ports should show as timed out or filtered, confirming the firewall is active.

---

## Reset Firewall (if needed)

```bash
sudo iptables -F
sudo iptables -X
sudo iptables -P INPUT ACCEPT
sudo iptables -P FORWARD ACCEPT
sudo iptables -P OUTPUT ACCEPT
```

---

## Observations & Learning

* Iptables can selectively block attacker IPs while allowing essential traffic.
* Default DROP policy ensures unknown/unwanted traffic is blocked.
* Verification with Nmap helps visualize active firewall rules.

---

## References

* [Iptables Documentation](https://linux.die.net/man/8/iptables)
* [Metasploitable2 Lab](https://sourceforge.net/projects/metasploitable/)

```

This version is **short, consistent with your other lab notes**, and ready to paste into GitHub.  

If you want, I can **combine this Firewall lab with your Nmap and Wireshark labs** into **one consolidated “Cybersecurity Labs – GitHub” Markdown** for all labs. Do you want me to do that?
```
