# Final Project: New Office Network Design — Fayetteville, NC
**IT-212 | Intro to Computer Networks | Grade: A**

## Scenario
Design a complete network for a new office opening in Fayetteville, NC. The office requires support for live video teleconferencing, efficient data transfer, wireless connectivity, remote access, and scalable growth — all with security built in from the ground up.

---

## 1. Internet Service Provider (ISP) Selection

### Options Evaluated
| ISP | Speed | Price/Month | SLA Uptime | Security Features |
|---|---|---|---|---|
| **AT&T Business Fiber** ✅ | Up to 1 Gbps | $170 | 99.9% guaranteed | Secure internet gateway, threat detection |
| Spectrum Business | 300 Mbps | $49 | 99.9% guaranteed | Basic |
| T1 Line | 1.544 Mbps | Higher | High | Dedicated |

### Recommendation: AT&T Business Fiber
**Rationale:** The office requires high bandwidth for live video teleconferencing and large data transfers. AT&T Business Fiber's 1 Gbps speeds, 99.9% SLA uptime guarantee, and built-in secure internet gateway and threat detection make it the best fit. While Spectrum Business is significantly cheaper, its 300 Mbps throughput is insufficient for the office's bandwidth needs during peak usage.

---

## 2. Physical Infrastructure

### Backbone
- **Fiber optic cables** — high speed, low latency, immune to electromagnetic interference; ideal for backbone between floors or main infrastructure runs

### Internal Wiring
- **Cat 6 / Cat 7 Ethernet** — high-speed connectivity to all workstations, printers, and wired devices; Cat 7 supports up to 10 Gbps over 100m

---

## 3. OSI Model Application

The OSI model guided every design decision — each layer has a corresponding hardware or software component in this design:

| Layer | Function | Implementation |
|---|---|---|
| **7 — Application** | Networking services for end users | Microsoft Teams (video conferencing, collaboration), email, file transfer |
| **6 — Presentation** | Data translation, encryption | TLS/SSL encryption for data in transit |
| **5 — Session** | Session management between devices | VPN sessions for remote workers |
| **4 — Transport** | Complete data transfer, error recovery, flow control | TCP for reliable transfer; UDP for real-time video |
| **3 — Network** | Routing and IP addressing | Routers directing packets across subnets |
| **2 — Data Link** | Node-to-node transfer, error correction | Managed switches, NICs |
| **1 — Physical** | Raw data transmission | Fiber optic backbone, Cat 6/7 Ethernet |

---

## 4. IP Addressing Strategy

### Recommendation: Class A Private Range — 10.0.0.0/8
**Rationale:**
- Provides 16+ million addresses — far exceeds current needs, accommodates years of growth
- Private IP space prevents direct external access (NAT required for internet)
- Single address space simplifies management — no complex subnetting required for initial deployment
- Avoids the limitations of smaller Class C ranges (254 hosts) that could require renumbering as the office grows

**Subnet allocation example:**
| Subnet | Range | Purpose |
|---|---|---|
| 10.0.1.0/24 | 10.0.1.1 – 10.0.1.254 | Employee workstations |
| 10.0.2.0/24 | 10.0.2.1 – 10.0.2.254 | Servers and printers |
| 10.0.3.0/24 | 10.0.3.1 – 10.0.3.254 | Guest wireless |
| 10.0.4.0/24 | 10.0.4.1 – 10.0.4.254 | VoIP / conferencing devices |

---

## 5. LAN Topology

### Recommended: Star Topology
A star topology connects all devices to a central switch — the most common and practical topology for office environments.

**Advantages:**
- Single device failure does not affect the rest of the network
- Easy to add new devices without disrupting existing connections
- Centralized management and troubleshooting at the switch level
- Highly scalable — additional switches can be added as the office grows

**Security advantage:** All traffic passes through a central point — ideal for traffic monitoring, VLAN segmentation, and access control enforcement.

---

## 6. Hardware Specifications

| Component | Recommended Device | Purpose |
|---|---|---|
| **Router** | Zyxel SCR 50AXE | High-performance routing, traffic management |
| **Managed Switches** | Netgear S8000 | Reliable wired LAN connectivity, VLAN support |
| **Wireless Access Points** | Cisco Meraki Go GR12 | High-density Wi-Fi for mobile devices |
| **Firewall** | Palo Alto Networks PA-800 series | Advanced threat prevention, application control |
| **VPN Gateway** | Secure VPN appliance | Encrypted remote access for employees |
| **Printers** | HP LaserJet Enterprise | Networked printing, high-volume, wireless capable |

### Software
- **Microsoft Windows Server** — network resource and service management
- **Microsoft Teams** — integrated meetings, calls, chat, and collaboration
- **PaperCut** — centralized print management, usage tracking, access control

---

## 7. Security Design

### Firewall (Palo Alto PA-800)
Next-generation firewall providing:
- Application-aware traffic inspection
- Intrusion prevention
- URL filtering
- Threat intelligence integration

### VPN Gateway
Secure encrypted tunnels for remote workers — all remote traffic encrypted before reaching the corporate network.

### Guest Network Isolation
Guest wireless (10.0.3.0/24) completely isolated from internal resources — guests can reach the internet but cannot access employee workstations, servers, or printers.

### Physical Security
- Cable management and locked server/network closet
- Access controls on network equipment rooms

---

## Key Takeaways
This project taught me that network design is never just technical — every decision (ISP, topology, IP addressing, hardware) has security, cost, and scalability implications that must be balanced against business requirements. A well-designed network builds security in from the ground up rather than adding it as an afterthought.

---

## Skills Demonstrated
`Network Design` `ISP Evaluation` `OSI Model` `IP Addressing (Class A)` `Subnetting Strategy` `Star Topology` `Hardware Selection` `Firewall Specification` `VPN Design` `Guest Network Isolation` `VLAN Planning` `Microsoft Teams` `Windows Server` `Technical Documentation`
