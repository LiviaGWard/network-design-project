# Milestone One: Key Considerations — New Office Network Design
**IT-212 | Intro to Computer Networks**

## Objective
Establish the foundational design decisions for the new office network — ISP type, physical cabling, OSI model mapping, hardware components, and IP addressing strategy.

---

## ISP Recommendation: Fiber Optic
Given the office's requirements for live video teleconferencing and efficient large-scale data transfer, **fiber optic** is the clear choice over cable or T1 options. Fiber provides:
- Highest bandwidth (1 Gbps+)
- Lowest latency — critical for real-time video
- Symmetric upload/download speeds — essential for video conferencing where both sending and receiving video streams simultaneously
- Superior reliability and resistance to interference

---

## Physical Cabling
- **Backbone:** Fiber optic — high speed, long distance, interference-immune
- **Internal:** Cat 6 or Cat 7 Ethernet — cost-effective, supports up to 10 Gbps at 100m

---

## OSI Model — Layer-by-Layer Design Mapping

| Layer | Hardware/Software | Role in This Network |
|---|---|---|
| Physical | Fiber optic, Cat 6/7 Ethernet | Raw signal transmission |
| Data Link | Switches, NICs | Node-to-node delivery, error correction |
| Network | Routers | IP routing and addressing |
| Transport | TCP/UDP | Reliable delivery (TCP) / Real-time streaming (UDP) |
| Session | VPN client/server | Session establishment and management |
| Presentation | TLS/SSL | Encryption and data formatting |
| Application | Teams, email, file transfer | End-user networking services |

---

## Core Hardware Components

| Device | Function |
|---|---|
| **Routers** | Direct data packets between networks |
| **Switches** | Connect devices within the LAN |
| **Wireless Access Points** | Provide Wi-Fi for mobile and wireless devices |
| **Firewalls** | Inspect and filter network traffic for security |
| **VPN Gateway** | Secure encrypted tunnel for remote access |

---

## IP Addressing: Class A Private Range (10.0.0.0/8)
- 16+ million addresses — scalable for any foreseeable growth
- Private range — not routable on the public internet (NAT required)
- Simplifies management — single contiguous address space for the entire office

---

## Skills Demonstrated
`OSI Model` `Fiber Optic Networking` `Ethernet Cabling` `IP Addressing` `Network Hardware` `VPN` `Firewall` `Network Design Fundamentals`
