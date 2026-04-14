# Module Four: Network Configuration Scavenger Hunt
**CYB-210 | Computer Networking**

## Objective
Use Cisco Packet Tracer CLI — not the GUI — to discover and document network configuration details across a live simulated network. This exercise mimics real-world network enumeration and assessment tasks.

---

## Why CLI Matters
Security professionals use CLI tools daily — for network auditing, incident response, and vulnerability assessment. Being comfortable navigating device configurations via command line is a fundamental skill that separates entry-level from mid-level practitioners.

---

## Wireless Routing Findings

| # | Objective | Finding |
|---|---|---|
| 1 | Wireless router IP address | **192.168.0.1** |
| 2 | DHCP scope starting IP | **192.168.0.115** |
| 3 | Guest wireless IPs available | **25** |
| 4 | Wireless device IP addresses | Laptop1: 192.168.0.116/24, Laptop0: 192.168.0.118/24, Tablet: 192.168.0.119/24 |
| 5 | Guest network name (SSID) | **FREE_WIRELESS** |
| 6 | Guest network security mode | **Disabled** ⚠️ |

### ⚠️ Security Finding: Guest Network Has No Encryption
The guest wireless network (FREE_WIRELESS) has its security mode set to **Disabled** — meaning all traffic is transmitted in plaintext with no WPA2/WPA3 encryption. This is a significant vulnerability:
- Any nearby device can capture guest network traffic
- Credentials, browsing activity, and data transmitted over the network are exposed
- Recommendation: Enable WPA2 or WPA3 with a strong passphrase, even for guest networks

---

## LAN Routing Findings
*Additional CLI findings documented from LAN routing segment — IP assignments, gateway configurations, and routing table entries verified across connected devices.*

---

## Skills Demonstrated
`Network Enumeration` `Cisco Packet Tracer CLI` `DHCP Analysis` `Wireless Security Assessment` `Network Auditing` `Security Finding Documentation`
