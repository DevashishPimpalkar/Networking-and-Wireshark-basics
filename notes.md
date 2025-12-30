# Networking & Wireshark – Study Notes

These notes document my hands-on learning of networking fundamentals
and packet analysis using Wireshark on Kali Linux.

The focus is on understanding how communication works at the packet level,
how attacks happen, and how they can be detected.

---

## 1. Networking Basics

### IP Addressing
- IPv4 addressing and subnet basics
- Private vs public IPs
- Gateway role in a network

### MAC Address
- Layer 2 hardware identifier
- Why MAC is used before IP (ARP dependency)
- One-to-one mapping inside a LAN

---

## 2. Core Protocols

### ARP (Address Resolution Protocol)
- Resolves IP → MAC inside local network
- Stateless protocol
- Vulnerable to spoofing

**Observed in Wireshark:**
- ARP request (Who has?)
- ARP reply (is at)

---

### DHCP (Dynamic Host Configuration Protocol)
- Automatically assigns:
  - IP address
  - Subnet mask
  - Gateway
  - DNS server

**DHCP Process (DORA):**
1. Discover
2. Offer
3. Request
4. Acknowledge

---

### DNS (Domain Name System)
- Resolves domain names to IP addresses
- UDP based (mostly)
- Target for spoofing and monitoring

---

## 3. Packet Analysis with Wireshark

### Capture Setup
- Interface selection
- Promiscuous mode
- Live capture vs offline PCAP analysis

### Useful Filters
- `arp`
- `dns`
- `dhcp`
- `tcp`
- `ip.addr == x.x.x.x`

---

## 4. TCP Flags (Handshake & Control)

- **SYN** → Connection request
- **SYN-ACK** → Server acknowledgment
- **ACK** → Connection established
- **RST** → Forceful connection reset
- **FIN** → Graceful connection close

---

## 5. Attacks & Network Abuse (Lab Understanding)

### ARP Poisoning / MITM
- Attacker impersonates gateway
- Enables traffic interception
- Visible via abnormal ARP traffic

### Rogue DHCP (Conceptual)
- Fake DHCP server responds faster than router
- Client receives attacker-controlled network config

---

## 6. Detection & Defensive Perspective

- ARP inspection
- DHCP snooping
- Monitoring duplicate IP/MAC behavior
- Suspicious packet timing and frequency

---

## 7. Learning Tools Used
- Kali Linux
- Wireshark
- Ettercap (lab environment only)

---

## 8. Learning Status
- Hands-on packet capture
- Reading protocol fields
- Statistics & conversation analysis
- Building strong networking foundation for cybersecurity
