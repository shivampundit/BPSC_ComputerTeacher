# Computer Networks (CN) — BPSC Computer Teacher Notes (Ultra Detailed & Comprehensive)

**Format:** Detailed Theory + Protocol Tables + OSI/TCP Layers + Formulas + Comparison Charts → Topic-wise MCQs (A–D) → Correct Option → Explanation

---

## 1. Introduction & Network Types

### What is a Computer Network?
A **Computer Network** is a collection of interconnected computing devices that share resources and exchange information. Networks enable:
- **Resource Sharing:** Printers, files, internet.
- **Communication:** Email, video conferencing.
- **Reliability:** Backup and redundancy.
- **Scalability:** Expanding connectivity.

### Basics
- **Computer Network:** Interconnected devices sharing resources.
- **Topology:** Physical/Logical arrangement (Bus, Star, Ring, Mesh, Tree, Hybrid).
- **Mode of Transmission:**
  - **Simplex:** One-way (TV, Keyboard → no feedback).
  - **Half-Duplex:** Both ways, but one at a time (Walkie-Talkie, CB radio).
  - **Full-Duplex:** Both ways simultaneously (Telephone, Internet, Ethernet).

### Network Types by Coverage Area
| Type | Coverage | Speed | Example | Technology |
|---|---|---|---|---|
| **PAN** (Personal) | meters (10m) | High | Bluetooth, Zigbee | Wireless |
| **LAN** (Local) | Building/Office | High (100-1000 Mbps) | Ethernet, WiFi | Wired/Wireless |
| **MAN** (Metropolitan) | City (10-50 km) | Medium | WiMAX, MPLS, Cable TV | Wireless/Fiber |
| **WAN** (Wide Area) | Country/Global | Low (Latency high) | Internet, MPLS | Leased Lines/Satellite |

### Network Topologies Detailed Comparison
| Topology | Physical Layout | Pros | Cons | Cabling | Failure Impact |
|---|---|---|---|---|---|
| **Mesh** | Every node connects to every other | Robust, Redundant, Secure | Expensive, Complex | n(n-1)/2 links | No single failure |
| **Star** | All nodes through central hub/switch | Easy to install, Manage, Scalable | Hub is SPOF, Extra latency | n links | Hub failure = all down |
| **Bus** | Linear, all on shared cable | Cheap, Efficient cabling | Collisions, Cable break = all down | 1 cable | One break kills all |
| **Ring** | Circular, point-to-point links | Deterministic, Token Ring access | Double failure tolerance | n links | One break = all down |
| **Tree** | Hierarchical (star + bus) | Scalable, Organized | Higher latency, Root failure | n links | Root failure critical |
| **Hybrid** | Combination of topologies | Flexible, Tailored | Complex design | Varies | Depends on design |

---

### MCQs (Section 1)

## Q1. Which topology requires the most amount of cabling?
A. Star
B. Mesh
C. Bus
D. Ring

> **Correct Option: B**
> **Explanation:** Mesh requires n(n-1)/2 links. For 5 devices: 5×4/2=10 cables.

## Q2. Walkie-Talkie is an example of:
A. Simplex
B. Half-Duplex
C. Full-Duplex
D. Multiplex

> **Correct Option: B**
> **Explanation:** Only one person can transmit at a time (push-to-talk mechanism).

## Q3. Which topology has a Single Point of Failure (SPOF)?
A. Mesh
B. Star
C. Ring
D. Bus

> **Correct Option: B**
> **Explanation:** Star topology fails completely if the central hub/switch fails.

---

## 2. OSI & TCP/IP Models (Detailed)

### OSI Model (7 Layers)
**Mnemonic:** "Please Do Not Throw Sausage Pizza Away"

| Layer | Name | Data Unit | Key Responsibility | Devices | Protocols |
|---|---|---|---|---|---|
| 7 | **Application** | Message/Data | User interface, User services, Encryption | N/A | HTTP, HTTPS, FTP, SMTP, POP3, IMAP, DNS, SSH, Telnet |
| 6 | **Presentation** | Data | Data formatting, Encryption/Decryption, Compression, Translation | N/A | SSL/TLS, JPEG, MPEG, ASCII |
| 5 | **Session** | Data | Session establishment, Maintenance, Termination, Synchronization | N/A | NetBIOS, RPC, PPTP, L2TP |
| 4 | **Transport** | Segment (TCP) / Datagram (UDP) | End-to-End delivery, Reliability, Flow Control, Error Checking | N/A | TCP, UDP, SCTP |
| 3 | **Network** | Packet | Routing, Logical Addressing (IP), Path determination | Router, Layer 3 Switch | IP (IPv4, IPv6), ICMP, IGMP, ARP, OSPF, RIP, BGP |
| 2 | **Data Link** | Frame | Physical Addressing (MAC), Framing, Error Detection, Flow Control | Switch, Bridge | Ethernet, PPP, Frame Relay, ATM |
| 1 | **Physical** | Bit | Bit transmission, Signaling, Cabling standards | Hub, Repeater, Modem | RJ45, Fiber Optic, Coaxial Cable, Wireless |

**Send/Receive Process:**
- **Send:** Application → Presentation → Session → **Transport (adds port)** → **Network (adds IP)** → **Data Link (adds MAC)** → Physical (bits).
- **Receive:** Physical (bits) → Data Link → Network → Transport → **Session** → Presentation → Application.

### TCP/IP Model (4 Layers) — Practical Internet Model
| Layer | OSI Equivalent | Function | Protocols |
|---|---|---|---|
| 4. **Application** | Layers 7, 6, 5 | User services, Encryption | HTTP, FTP, SMTP, DNS |
| 3. **Transport** | Layer 4 | End-to-End delivery | TCP, UDP |
| 2. **Internet** | Layer 3 | Routing, IP addressing | IP, ICMP, ARP |
| 1. **Network Access/Link** | Layers 2, 1 | Hardware, Cabling | Ethernet, PPP |

### Comparison: OSI vs TCP/IP
| Aspect | OSI | TCP/IP |
|---|---|---|
| **Layers** | 7 | 4 |
| **Development** | ISO (1984) | ARPA (1970s) |
| **Theoretical** | Yes | Practical |
| **Usage** | Learning, Reference | Internet standard |
| **Adoption** | Limited | Universal |

---

### MCQs (Section 2)

## Q4. Which OSI layer is responsible for end-to-end delivery and flow control?
A. Network
B. Transport
C. Data Link
D. Session

> **Correct Option: B**
> **Explanation:** Transport layer (Layer 4) uses TCP/UDP for reliability and flow control.

## Q5. Routers operate at which layer of the OSI model?
A. Layer 2 (Data Link)
B. Layer 3 (Network)
C. Layer 4 (Transport)
D. Layer 1 (Physical)

> **Correct Option: B**
> **Explanation:** Routers use IP addresses to make routing decisions.

## Q6. Which device operates at Layer 2 and learns MAC addresses?
A. Router
B. Hub
C. Switch
D. Repeater

> **Correct Option: C**
> **Explanation:** Switches build MAC tables and forward frames based on MAC addresses.

---

## 3. Data Link Layer (DLL) — Detailed

### Key Responsibilities
1. **Framing:** Breaking data into frames with headers/trailers.
2. **Physical Addressing:** Using MAC (Media Access Control) addresses (48-bit, hex format: AA:BB:CC:DD:EE:FF).
3. **Error Detection:** CRC (Cyclic Redundancy Check), Checksum, Parity.
4. **Flow Control:** Managing transmission rate (Stop & Wait, Sliding Window).
5. **Access Control:** CSMA/CD, CSMA/CA, Token Ring.

### Sublayers
- **LLC (Logical Link Control):** Interface between Network layer and MAC sublayer.
- **MAC (Media Access Control):** Direct hardware access, frame formatting.

### Error Detection vs Error Correction
| Technique | Type | Method | Capability |
|---|---|---|---|
| **Parity Bit** | Detection | Even/Odd bit addition | Detects 1-bit error (not always) |
| **Checksum** | Detection | Sum modulo arithmetic | Detects many errors |
| **CRC** | Detection | Polynomial division | Detects burst errors |
| **Hamming Code** | Correction | Distance 3+ | Corrects 1-bit errors |

### Medium Access Control Protocols
| Protocol | Type | Description | Efficiency | Medium |
|---|---|---|---|---|
| **Pure ALOHA** | Random | Transmit anytime; If collision, retransmit | 18.4% | Wireless |
| **Slotted ALOHA** | Random (Synchronized) | Transmit in time slots | 36.8% | Wireless |
| **CSMA/CD** | Deterministic | Carrier sense, Collision Detection | ~100% at low load | Wired (Ethernet) |
| **CSMA/CA** | Deterministic | Carrier sense, Collision Avoidance (RTS/CTS) | ~90% | Wireless (WiFi) |
| **Token Ring** | Deterministic | Token circulation, Ordered access | Guaranteed slot | Ring topology |

---

### MCQs (Section 3)

## Q7. The MAC address size is:
A. 32 bits
B. 48 bits
C. 64 bits
D. 128 bits

> **Correct Option: B**
> **Explanation:** MAC address is 48-bit (6 bytes), represented as AA:BB:CC:DD:EE:FF.

## Q8. Which protocol is used in wired Ethernet to handle collisions?
A. CSMA/CA
B. CSMA/CD
C. ALOHA
D. Token Passing

> **Correct Option: B**
> **Explanation:** CSMA/CD detects collision and immediately stops transmission (wired only).

## Q9. CRC is primarily used for:
A. Error Correction
B. Error Detection
C. Encryption
D. Flow Control

> **Correct Option: B**
> **Explanation:** CRC detects burst errors but doesn't correct them.

---

## 4. Network Layer (IP Addressing, Subnetting, Routing)

### IPv4 Addressing Detailed
- **Total bits:** 32
- **Format:** Decimal dotted notation (192.168.1.1)
- **Range:** 0.0.0.0 to 255.255.255.255

### Classful IP Addressing (Legacy)
| Class | 1st Byte Range | Network Bits | Host Bits | Default Mask | Use | Number |
|---|---|---|---|---|---|---|
| **A** | 1 – 126 | 8 (/8) | 24 | 255.0.0.0 | Large networks | 128 (0 reserved) |
| **B** | 128 – 191 | 16 (/16) | 16 | 255.255.0.0 | Medium networks | 16,384 |
| **C** | 192 – 223 | 24 (/24) | 8 | 255.255.255.0 | Small networks (LANs) | 2,097,152 |
| **D** | 224 – 239 | N/A | N/A | N/A | Multicast | 268,435,456 |
| **E** | 240 – 255 | N/A | N/A | N/A | Experimental | Reserved |

### Private IP Ranges (RFC 1918)
| Class | Private Range | Use |
|---|---|---|
| **A** | 10.0.0.0 – 10.255.255.255 | Large LANs, Enterprises |
| **B** | 172.16.0.0 – 172.31.255.255 | Medium LANs |
| **C** | 192.168.0.0 – 192.168.255.255 | Small LANs, Home Networks |

### Special IP Addresses
| Address | Purpose |
|---|---|
| 127.0.0.1 / 127.0.0.0/8 | Loopback (Localhost testing) |
| 255.255.255.255 | Broadcast (Limited) |
| 0.0.0.0 | This network / Default route |
| 169.254.0.0/16 | Link-local (APIPA) |
| 224.0.0.0/4 | Multicast |

### Subnetting (CIDR - Classless Inter-Domain Routing)
- **Concept:** Borrowing host bits for network bits.
- **/24** = 24 network bits, 8 host bits.
- **Hosts per subnet:** 2^(host bits) − 2
- **Subnets available:** 2^(borrowed bits)

### Network Layer Protocols
| Protocol | Purpose | Example |
|---|---|---|
| **IP (IPv4/IPv6)** | Routing, Logical addressing | 192.168.1.1 |
| **ARP** | IP → MAC resolution | Find MAC for known IP |
| **RARP** | MAC → IP (Obsolete) | Replaced by DHCP |
| **ICMP** | Error reporting, Diagnostics | Ping, Traceroute |
| **IGMP** | Multicast group management | Join/Leave multicast |
| **NAT** | Network Address Translation | Private ↔ Public IP |

### Routing Algorithms
| Algorithm | Category | Basis | Convergence | Example |
|---|---|---|---|---|
| **RIP** | Distance Vector | Hop count (Max 15) | Slow (Count-to-infinity) | RIPv1, RIPv2 |
| **OSPF** | Link State | Shortest path (Dijkstra) | Fast | Modern networks |
| **BGP** | Path Vector | AS paths | Policy-based | Internet backbone |
| **EIGRP** | Advanced Distance Vector | Multiple metrics | Fast | Cisco networks |

---

### MCQs (Section 4)

## Q10. 127.0.0.1 is a:
A. Private IP
B. Loopback Address
C. Multicast Address
D. Broadcast Address

> **Correct Option: B**
> **Explanation:** Used for testing network card/software locally (localhost).

## Q11. Which protocol maps IP address to MAC address?
A. RARP
B. DNS
C. ARP
D. DHCP

> **Correct Option: C**
> **Explanation:** ARP (Address Resolution Protocol) finds MAC for a known IP.

## Q12. How many usable hosts are there in a /26 subnet?
A. 62
B. 64
C. 256
D. 128

> **Correct Option: A**
> **Explanation:** /26 means 6 host bits: 2^6 = 64, minus 2 (network & broadcast) = 62.

---

## 5. Transport Layer (TCP & UDP)

### TCP (Transmission Control Protocol) — Detailed
- **Connection-oriented:** Requires establishment.
- **Reliable:** ACK-based (Positive acknowledgment with retransmission).
- **Ordered:** Sequence numbers ensure order.
- **Flow Control:** Sliding window prevents receiver overload.
- **Congestion Control:** Slow Start, Congestion Avoidance (AIMD).
- **Header Size:** 20 bytes (minimum).
- **Used in:** HTTP, HTTPS, FTP, SMTP, SSH.

### TCP Three-Way Handshake (Connection Establishment)
1. **SYN:** Client sends synchronization sequence number.
2. **SYN-ACK:** Server acknowledges and sends own sequence number.
3. **ACK:** Client acknowledges server's sequence number.

### TCP Connection Termination (Four-Way Handshake)
- **FIN:** Initiator sends finish.
- **ACK:** Receiver acknowledges.
- **FIN:** Receiver sends finish.
- **ACK:** Initiator acknowledges.

### UDP (User Datagram Protocol) — Detailed
- **Connectionless:** No handshake.
- **Unreliable:** No ACKs, No retransmission (Best-effort).
- **Fast:** Low overhead (8-byte header vs TCP 20-byte).
- **Stateless:** Each datagram independent.
- **Used in:** DNS, DHCP, VoIP, Video Streaming, Gaming, Online multiplayer.

### TCP vs UDP
| Feature | TCP | UDP |
|---|---|---|
| **Connection** | Required (3-way) | None |
| **Reliability** | Guaranteed in-order | Best-effort |
| **Overhead** | High (ACKs, Sequencing) | Low |
| **Speed** | Slower | Faster |
| **Error Control** | Checksum + Retransmit | Checksum only |
| **Flow Control** | Yes (Sliding Window) | No |
| **Applications** | Email, Web, File Transfer | Streaming, Gaming, DNS |

### Well-Known Ports
| Port | Protocol | Service | Security |
|---|---|---|---|
| 20/21 | FTP | File Transfer | Unencrypted |
| 22 | SSH | Secure Shell | Encrypted |
| 23 | Telnet | Remote Login | Unencrypted (obsolete) |
| 25 | SMTP | Email Sending | Unencrypted |
| 53 | DNS | Domain Names | UDP/TCP |
| 80 | HTTP | Web | Unencrypted |
| 110 | POP3 | Email Retrieval | Unencrypted |
| 143 | IMAP | Email Retrieval | Unencrypted |
| 443 | HTTPS | Secure Web | TLS/SSL Encrypted |
| 3306 | MySQL | Database | Unencrypted |
| 5432 | PostgreSQL | Database | Unencrypted |

---

### MCQs (Section 5)

## Q13. Which protocol guarantees reliable and ordered delivery?
A. IP
B. UDP
C. TCP
D. ICMP

> **Correct Option: C**
> **Explanation:** TCP ensures reliability via sequence numbers and ACKs.

## Q14. The standard port for HTTPS is:
A. 21
B. 25
C. 80
D. 443

> **Correct Option: D**
> **Explanation:** Port 443 is HTTPS (Secure HTTP with TLS).

## Q15. UDP header size is:
A. 8 bytes
B. 20 bytes
C. 32 bytes
D. 16 bytes

> **Correct Option: A**
> **Explanation:** UDP has minimal overhead (8 bytes), making it faster than TCP (20 bytes).

---

## 6. Application Layer (DNS, DHCP, HTTP, Email)

### DNS (Domain Name System)
- **Purpose:** Translates domain names (www.example.com) to IP addresses.
- **Hierarchy:** Root → TLD (.com, .org) → Authoritative servers.
- **Port:** 53 (UDP for queries, TCP for zone transfers).
- **Types:** A (IPv4), AAAA (IPv6), MX (Mail), CNAME (Alias), NS (Nameserver).

### DHCP (Dynamic Host Configuration Protocol)
- **Purpose:** Automatic IP assignment.
- **Process (DORA):**
  1. **Discover:** Client broadcasts for DHCP server.
  2. **Offer:** Server offers IP, Gateway, DNS.
  3. **Request:** Client requests offered IP.
  4. **Acknowledge:** Server confirms assignment.
- **Port:** 67 (Server), 68 (Client).

### HTTP/HTTPS
- **HTTP:** Stateless, Request-Response, Port 80.
- **HTTPS:** HTTP over SSL/TLS (Encryption), Port 443.
- **Methods:** GET (Retrieve), POST (Submit), PUT (Update), DELETE, HEAD.
- **Status Codes:** 2xx (Success), 3xx (Redirect), 4xx (Client error), 5xx (Server error).

### Email Protocols
| Protocol | Port | Purpose | Security |
|---|---|---|---|
| **SMTP** | 25/587 | Sending mail | Unencrypted/Encrypted |
| **POP3** | 110/995 | Receiving (Download) | Unencrypted/SSL |
| **IMAP** | 143/993 | Receiving (Sync) | Unencrypted/SSL |

---

### MCQs (Section 6)

## Q16. Which protocol uses the DORA process?
A. DNS
B. DHCP
C. FTP
D. SMTP

> **Correct Option: B**
> **Explanation:** DHCP uses Discover, Offer, Request, Acknowledge for IP assignment.

## Q17. DNS primarily uses which transport protocol?
A. TCP
B. UDP
C. ICMP
D. IGMP

> **Correct Option: B**
> **Explanation:** DNS queries use UDP 53 for speed; TCP used for zone transfers.

---

## 7. Network Security & Cryptography

### Cryptography Types
| Type | Key Model | Speed | Use |
|---|---|---|---|
| **Symmetric** | Shared secret key | Fast | Bulk encryption (AES, DES) |
| **Asymmetric** | Public/Private pair | Slow | Key exchange, Digital signatures (RSA) |
| **Hash** | One-way function | Fast | Integrity verification (MD5, SHA-1, SHA-256) |

### Firewalls & Security
- **Firewall:** Packet filtering, Stateful inspection, Proxy services.
- **Intrusion Detection System (IDS):** Monitors traffic for threats.
- **VPN:** Virtual Private Network, Encryption over public internet.

---

### MCQs (Section 7)

## Q18. Which cryptography method is used for digital signatures?
A. Symmetric Key
B. Asymmetric Key
C. Hash Function
D. Checksum

> **Correct Option: B**
> **Explanation:** Asymmetric (Public/Private) allows digital signatures and authentication.

---

## 8. Key Concepts & Formulas

### Address Calculation
- **Network Address:** AND IP with Subnet Mask.
- **Broadcast Address:** Set all host bits to 1.
- **First Usable IP:** Network Address + 1.
- **Last Usable IP:** Broadcast Address − 1.

### Bandwidth & Latency
- **Throughput:** Actual data rate (less than bandwidth due to overhead).
- **Latency:** Delay in transmission.
- **Bandwidth-Delay Product:** BW × RTT (amount of data in transit).

---

## End of Ultra Detailed CN Notes
