# Module Two: Packet Tracer Connectivity Lab
**CYB-210 | Computer Networking**

## Objective
Build a basic network in Cisco Packet Tracer and verify end-to-end connectivity between devices using ping tests.

---

## What I Did
Constructed a simulated network with multiple devices and verified that each could communicate with the others by running ping tests across three separate connections.

## Ping Test Results
All three ping tests returned successful replies after initial ARP resolution:
- **Ping 1:** ✅ Successful — device-to-device connectivity confirmed
- **Ping 2:** ✅ Successful — cross-segment communication verified
- **Ping 3:** ✅ Successful — full network reachability confirmed

> Note: The first ICMP packet in Packet Tracer often times out while ARP resolves the MAC address. Subsequent packets succeed — this is expected behavior, not a configuration error.

---

## Key Concepts Applied
- Network device placement and cabling
- IP address assignment
- ARP (Address Resolution Protocol) — how devices resolve IP to MAC addresses
- ICMP ping — the standard tool for verifying network connectivity
- Reading ping output to confirm successful communication

---

## Skills Demonstrated
`Cisco Packet Tracer` `Network Construction` `Ping Testing` `ARP` `ICMP` `Connectivity Verification`
