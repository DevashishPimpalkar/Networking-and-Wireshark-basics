## HTTP Packet Analysis (Wireshark)

### What is HTTP?
HTTP (Hypertext Transfer Protocol) is a stateless, application-layer protocol used for communication between a client and a server.  
It typically runs over TCP port 80 and transmits data in plain text.

---

### Observations from Wireshark
- Client initiates a TCP connection to the server
- HTTP requests such as GET and POST are visible
- Request and response headers are readable in plain text
- Server responds with status codes and data payload

---

### Key Fields Observed
- Request Method (GET / POST)
- Host (domain name)
- User-Agent (browser and OS details)
- Status Code (200, 301, 404, etc.)
- Content-Type (type of response data)

---

### Security Insight
HTTP traffic is not encrypted.  
Any attacker on the same network can inspect requests, responses, and sensitive information.

This is why HTTPS is preferred over HTTP.

---

### Wireshark Filters Used
http  
tcp.port == 80

---

### Learning Outcome
- Understood how web communication works at packet level
- Observed unencrypted data transmission
- Built a foundation for understanding HTTPS and TLS

---

### Next Step
Analyze HTTPS traffic and observe TLS handshake behavior.
