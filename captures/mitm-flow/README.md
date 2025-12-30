## Man-In-The-Middle (MITM) Attack Flow

### What is MITM?
MITM is an attack where the attacker positions themselves between two communicating parties without their knowledge.

Both sides believe they are talking directly to each other.

---

### Typical MITM Flow
1. Victim connects to network
2. Attacker gains position (ARP poisoning / Rogue DHCP)
3. Traffic flows through attacker
4. Attacker observes, modifies, or blocks packets

---

### Techniques Used
- ARP Poisoning
- Rogue DHCP
- DNS Spoofing
- SSL stripping (HTTP only)

---

### What Can Be Observed
- Source and destination IPs
- Protocols used
- Packet size and timing
- Unencrypted payloads (HTTP)

---

### What Cannot Be Observed
- HTTPS content
- Encrypted credentials
- TLS application data

---

### Defender Insight
MITM works because of:
- Trust-based protocols
- Weak network validation
- User unawareness

---

### Learning Outcome
- Understood full attack chain
- Learned attacker vs defender perspective
- Realized MITM is about **control, not brute force**

---

### Hacker Mindset
Don’t attack people.
Attack infrastructure trust.
