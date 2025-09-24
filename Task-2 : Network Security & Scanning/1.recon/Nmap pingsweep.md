# Nmap Ping Sweep Notes
- Command used: nmap -sP 192.168.56.0/24
- Purpose: To **discover which hosts are alive** in the target network (host discovery).

## Output Explanation:
- Nmap scan report for 192.168.56.1
  - Host is up (0.00023s latency) → This IP responded to ping.
  - MAC Address: BA:00:27:00:00:04 → Physical address of the device, vendor unknown.
- Nmap scan report for 192.168.56.100
  - Host is up (8.00030s latency) → Another active host.
  - MAC Address: 08:00:27:89:88:A7 → Shows it’s a VirtualBox VM NIC (Metasploitable/Kali)
- Nmap scan report for 192.168.56.105
  - Host is up → Another active VM in network.

- Nmap done: 256 IP addresses scanned → Found 3 hosts alive in the network.

## Why Important:
- Step 1 for **network reconnaissance**: attackers need to know which hosts exist before scanning ports/services.
- Identifies active devices in a subnet.
- Helps narrow down targets for port scanning and vulnerability assessment.
