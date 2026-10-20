# Computer Networks (CN) Cheatsheet 🌐

## 1. OSI vs. TCP/IP Model
| Layer | OSI | TCP/IP | Protocols / Hardware |
|---|---|---|---|
| 7 | Application | Application | HTTP, HTTPS, DNS, FTP, SMTP, SSH |
| 6 | Presentation | Application | SSL/TLS, ASCII, JPEG |
| 5 | Session | Application | NetBIOS, RPC, Sockets |
| 4 | Transport | Transport | TCP, UDP |
| 3 | Network | Internet | IP, ICMP, ARP, Routers |
| 2 | Data Link | Network Access | Ethernet, Wi-Fi, MAC addresses, Switches |
| 1 | Physical | Network Access | Cables, Fiber Optics, Hubs |

## 2. TCP vs. UDP
| Feature | TCP | UDP |
|---|---|---|
| **Connection** | Connection-oriented (3-way handshake) | Connectionless |
| **Reliability** | Guaranteed delivery (retransmission, checksums) | Unreliable (fire and forget) |
| **Ordering** | In-order sequence delivery | Packets can arrive out-of-order |
| **Flow/Congestion Control** | Sliding window, AIMD, Slow Start | None |
| **Header Size** | 20–60 bytes | 8 bytes |
| **Use cases** | Web browsing, file transfer, email | Video streaming, online gaming, DNS, VoIP |

## 3. TCP 3-Way Handshake & 4-Way Termination
- **Connection Establishment:**
  1. Client $\to$ Server: `SYN` (seq = x)
  2. Server $\to$ Client: `SYN-ACK` (seq = y, ack = x + 1)
  3. Client $\to$ Server: `ACK` (seq = x + 1, ack = y + 1)
- **Connection Termination:**
  1. Client $\to$ Server: `FIN`
  2. Server $\to$ Client: `ACK`
  3. Server $\to$ Client: `FIN`
  4. Client $\to$ Server: `ACK` (Client enters `TIME_WAIT` state for $2 \times \text{MSL}$)

## 4. What Happens When You Type a URL in a Browser?
1. **URL Parsing:** Browser extracts protocol (`https`), domain (`example.com`), and port (`443`).
2. **DNS Resolution:** Browser cache $\to$ OS cache $\to$ Router cache $\to$ ISP Resolver $\to$ Root $\to$ TLD $\to$ Authoritative DNS.
3. **TCP Handshake:** Client establishes TCP connection with resolved IP on port 443.
4. **TLS/SSL Handshake:** Cipher negotiation, server certificate verification, session key exchange.
5. **HTTP Request & Response:** Browser sends `GET /`, server processes and responds with `200 OK` HTML payload.
6. **Rendering Engine:** Browser parses HTML $\to$ DOM tree, CSS $\to$ CSSOM, executes JS, and renders the view.
