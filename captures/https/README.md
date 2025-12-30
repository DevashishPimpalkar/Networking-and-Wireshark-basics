## HTTPS Packet Analysis (Wireshark)

### What is HTTPS?
HTTPS (Hypertext Transfer Protocol Secure) is HTTP over TLS/SSL.  
It encrypts communication between client and server to ensure confidentiality, integrity, and authentication.

It typically runs over TCP port 443.

---

### Observations from Wireshark
- TCP three-way handshake occurs first
- TLS handshake follows (Client Hello, Server Hello, Certificates)
- After handshake, application data is encrypted
- HTTP content is NOT visible in plain text

---

### Key TLS Components Observed
- Client Hello (supported cipher suites, TLS version)
- Server Certificate (used for authentication)
- Key Exchange process
- Encrypted Application Data

---

### What Cannot Be Seen (Important)
- URLs beyond domain
- Request body
- Login credentials
- Response content

Only metadata like IPs, ports, packet sizes, and timing are visible.

---

### Security Insight
HTTPS protects against:
- Packet sniffing
- Credential theft
- MITM attacks (without certificate compromise)

However, attackers can still observe traffic patterns and endpoints.

---

### Wireshark Filters Used
tls  
tcp.port == 443

---

### Learning Outcome
- Understood difference between HTTP and HTTPS
- Observed TLS handshake process
- Learned why HTTPS is critical for secure communication

---

### Attacker Perspective
Even when data is encrypted:
- Traffic flow
- Endpoints
- Timing patterns  
can still reveal valuable intelligence.

---

### Next Step
Study TLS handshake deeply and explore certificate-based attacks and MITM scenarios.
