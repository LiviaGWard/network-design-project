# Project Two: Network Design Rationale
**CYB-210 | Computer Networking | Grade: A**

## Objective
Design a multi-network architecture to safely onboard new employees and their devices onto an isolated network (Network3) while maintaining controlled communication with the existing production network (NetworkA).

---

## Network Design Overview

| Network | IP Range | Purpose |
|---|---|---|
| **NetworkA** | 192.168.1.x | Existing production network |
| **Network3** | 10.0.0.x | Isolated new employee network |

---

## Design Decisions & Rationale

### 1. Network Isolation
New employees' devices were placed on Network3 rather than NetworkA to protect the integrity of existing systems. Their older hardware may carry unpatched vulnerabilities or misconfigurations — isolating them prevents those risks from directly affecting the production network.

> *Security principle: Never trust unvetted devices. Isolate first, verify before granting access.*

---

### 2. IP Addressing
- **NetworkA:** 192.168.1.x address space
- **Network3:** 10.0.0.x address space

Using non-overlapping address ranges prevents IP conflicts and makes routing decisions clear and deliberate. Any traffic crossing between networks must pass through a router — providing a natural inspection point.

---

### 3. Subnet Masks
Both networks use a **255.255.255.0** (/24) subnet mask, allowing up to 254 hosts per network. This enforces a clean boundary — devices outside the subnet must go through the router to communicate, preventing direct cross-network access.

---

### 4. Static Routing
Routers in both NetworkA and Network3 were configured with static routes pointing to each other. This allows controlled, deliberate communication between the two networks without enabling full open routing.

**Why static over dynamic here:** In this scenario, static routing provides predictability and control — the routing table only contains what was explicitly configured, reducing attack surface compared to dynamic routing protocols that auto-discover neighbors.

---

### 5. DHCP Configuration
DHCP was configured on NetworkA to automatically assign IP addresses. This ensures that any device temporarily moved from Network3 to NetworkA receives a valid IP without manual configuration — reducing human error and administrative overhead.

---

### 6. NAT / PAT
NAT (Network Address Translation) was implemented to:
- Mask internal IP addresses from external networks
- Allow both NetworkA and Network3 devices to access external resources through a single public-facing address
- Add a layer of obscurity — internal network topology is not exposed

PAT (Port Address Translation) extends this by mapping multiple internal connections to a single external IP using port numbers.

---

## Network Diagram
*See `CYB210 Project Two diagram Livia Ward.png` in this repository for the full network topology.*

---

## Skills Demonstrated
`Multi-Network Architecture` `Static Routing` `IPv4 Addressing` `Subnetting` `DHCP Configuration` `NAT/PAT` `Network Security Rationale` `Cisco Packet Tracer` `Technical Documentation`
