## Rogue DHCP Attack (Wireshark / Ettercap)

### What is Rogue DHCP?
Rogue DHCP is an attack where a malicious device responds to DHCP requests faster than the legitimate router.

The victim unknowingly receives:
- Fake IP configuration
- Attacker-controlled gateway
- Attacker-controlled DNS server

---

### Normal vs Rogue DHCP
- Legitimate DHCP: Router assigns IP, gateway, DNS
- Rogue DHCP: Attacker assigns IP before router

Trust is broken at the infrastructure level.

---

### Observations
- DHCP Discover broadcast from victim
- Rogue DHCP Offer received first
- Victim accepts attacker’s configuration
- All traffic flows through attacker

---

### Why This Works
DHCP has **no authentication**.  
Client trusts whoever responds first.

---

### Security Impact
- Enables MITM attacks
- DNS spoofing possible
- Traffic redirection
- Credential interception (on HTTP)

---

### Learning Outcome
- Understood DHCP trust weakness
- Learned how infrastructure attacks work
- Realized attacks target **systems, not people**

---

### Key Insight
Trust is built.
So is misuse.
