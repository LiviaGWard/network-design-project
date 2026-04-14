# 🌐 CYB-210: Computer Networking
**Southern New Hampshire University | Grade: A | Term: 2024 C-5 (Sep – Oct)**

> Hands-on computer networking course covering IP addressing, subnetting, DHCP, NAT/PAT, VLAN configuration, static routing, and secure network design — all built and tested in Cisco Packet Tracer.

---

## 📋 Course Overview
This course went far beyond theory — every concept was applied hands-on in Cisco Packet Tracer, building and configuring real simulated networks. From basic connectivity to multi-network routing with NAT/PAT and VLAN segmentation, this course gave me practical skills I use directly in a security operations context.

---

## 📁 Repository Structure

```
network-design-project/
│
├── projects/
│   ├── project-one-network-reconfiguration.md
│   └── project-two-network-design-rationale.md
│
├── activities/
│   ├── module-two-packet-tracer-connectivity.md
│   ├── module-three-subnetting-practice.md
│   ├── module-four-network-scavenger-hunt.md
│   └── module-five-rip-nat-configuration.md
│
└── README.md
```

> 📎 **Note:** Original Cisco Packet Tracer (.pkt) files are included in this repository. To open them, download [Cisco Packet Tracer](https://www.netacad.com/courses/packet-tracer) (free with Cisco NetAcad account).

---

## 📝 Projects

### 🔵 Project One — Network Reconfiguration (VLAN & Segmentation)
Reconfigured an existing network in Cisco Packet Tracer to implement proper segmentation using VLANs, a guest wireless network, device isolation, and camera network separation.

**Key tasks:**
- Configured VLANs to segment traffic by department/function
- Set up a guest wireless network isolated from the main LAN
- Reconfigured device placement for proper network isolation
- Added and segmented a camera network
- Documented network segregation rationale

**Skills demonstrated:** VLAN configuration, network segmentation, wireless networking, security-driven network design

---

### 🔵 Project Two — Network Design Rationale (Multi-Network with NAT/PAT)
Designed and documented a full multi-network architecture to onboard new employees onto an isolated network (Network3) while maintaining controlled communication with the existing network (NetworkA).

**Key design decisions:**
- **Network isolation:** New devices placed on Network3 (10.0.0.x) to protect main network
- **Static routing:** Both routers configured with static routes for controlled inter-network communication
- **IP addressing:** NetworkA (192.168.1.x) and Network3 (10.0.0.x) — no conflicts
- **Subnetting:** 255.255.255.0 masks enforce clean network boundaries
- **DHCP:** Configured on NetworkA for automatic IP assignment
- **NAT/PAT:** Internal IPs masked; external communication secured

**Skills demonstrated:** Multi-network architecture, static routing, IP addressing, subnetting, DHCP, NAT/PAT, security documentation

---

## 🗂️ Activities

### Module Two — Packet Tracer Connectivity Lab
Built a basic network and verified connectivity using ping tests across three connections. Confirmed successful packet transmission with screenshots.

### Module Three — Subnetting Practice
Completed five subnetting exercises calculating network addresses, subnet masks, host ranges, and broadcast addresses. Subnetting is foundational to security — it defines which devices can communicate directly and which must pass through a router.

### Module Four — Network Configuration Scavenger Hunt
Used Cisco Packet Tracer CLI to enumerate a live simulated network — discovering IP addresses, DHCP scope, wireless configuration, and security settings without using GUI shortcuts.

| Objective | Finding |
|---|---|
| Wireless router IP | 192.168.0.1 |
| DHCP scope start | 192.168.0.115 |
| Guest IPs available | 25 |
| Guest network name | FREE_WIRELESS |
| Guest security mode | Disabled ⚠️ (flagged as risk) |

### Module Five — RIP Routing & NAT Configuration
Configured a router via CLI to implement RIP dynamic routing and NAT on a restructured network. Troubleshot interface naming errors using `show ip interface brief`. Verified full connectivity with ping tests after configuration.

---

## 💡 Key Concepts Mastered
- IPv4 addressing and subnet mask calculation
- VLAN configuration and network segmentation
- Static and dynamic routing (RIP)
- DHCP server configuration
- NAT and PAT implementation
- Guest wireless setup and security risks
- Cisco Packet Tracer — CLI and GUI configuration
- Multi-network architecture and documentation
- Network troubleshooting methodology

---

## 🛠️ Tools Used
- **Cisco Packet Tracer** — all labs and projects
- **Router/Switch CLI** — direct command-line configuration

## 📚 Course
- **CYB-210** — Computer Networking | Grade: A | SNHU 2024
