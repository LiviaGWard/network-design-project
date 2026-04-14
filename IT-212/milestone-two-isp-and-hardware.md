# Milestone Two: ISP Selection & Hardware Configuration
**IT-212 | Intro to Computer Networks**

## Objective
Finalize ISP selection with real-world vendor research, specify hardware and software solutions, and design printer/peripheral configuration for the new office.

---

## ISP Comparison — Fayetteville, NC

| Factor | AT&T Business Fiber ✅ | Spectrum Business |
|---|---|---|
| **Speed** | Up to 1 Gbps | 300 Mbps |
| **Price** | $170/month | $49/month |
| **Uptime SLA** | 99.9% guaranteed | 99.9% guaranteed |
| **Security** | Secure internet gateway + threat detection | Basic |
| **Best for** | High bandwidth, security-conscious businesses | Cost-sensitive, lower bandwidth needs |

### Decision: AT&T Business Fiber
The $121/month premium over Spectrum is justified by:
- 3.3× the bandwidth — essential for simultaneous video teleconferencing across multiple rooms
- Built-in threat detection — reduces security tool overhead
- SLA-backed reliability — business operations depend on consistent uptime

---

## Hardware Specifications

### Routing & Switching
| Device | Model | Reason Selected |
|---|---|---|
| Router | Zyxel SCR 50AXE | High performance, supports advanced traffic management |
| Managed Switch | Netgear S8000 | Enterprise-grade, VLAN support, reliable LAN connectivity |

### Wireless
| Device | Model | Reason Selected |
|---|---|---|
| Wireless Access Points | Cisco Meraki Go GR12 | High-density, cloud-managed, ideal for mobile device environments |

### Security
| Device | Model | Reason Selected |
|---|---|---|
| Firewall | Palo Alto Networks PA-800 Series | Next-gen firewall with application control, IPS, and threat intelligence |
| VPN Gateway | Secure VPN appliance | Encrypted remote access for off-site employees |

---

## Software Stack
| Software | Purpose |
|---|---|
| Microsoft Windows Server | Network resource management, Active Directory, DNS/DHCP |
| Microsoft Teams | Integrated video conferencing, calls, chat, and file sharing |
| PaperCut | Centralized print management — usage tracking, access control, driver distribution |

---

## Printer Configuration

### Recommended: HP LaserJet Enterprise
- Supports both wireless and wired network printing
- High-volume capability for office scale
- Compatible with PaperCut for centralized management

### Print Management Strategy
- **PaperCut** tracks usage per user/department — enables cost allocation and quota enforcement
- **Centralized driver management** — automatic driver distribution and updates eliminate manual IT intervention per device
- **Access control** — restrict color printing, limit print quotas, require authentication at the printer (follow-me printing)

**Security benefit:** Centralized print management prevents sensitive documents from being left uncollected at printers — a common but overlooked data leakage vector.

---

## Skills Demonstrated
`ISP Evaluation & Selection` `Vendor Research` `Hardware Specification` `Cisco Meraki` `Palo Alto Firewall` `Windows Server` `Microsoft Teams` `Print Management` `PaperCut` `Network Security Planning` `Cost-Benefit Analysis`
