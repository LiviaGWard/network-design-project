# Module Three: Subnetting Practice
**CYB-210 | Computer Networking**

## Objective
Complete five subnetting exercises calculating network addresses, usable host ranges, subnet masks, and broadcast addresses for given IP blocks.

---

## Why Subnetting Matters for Security
Subnetting is not just a networking skill — it is a security tool. Every subnet creates a boundary. Devices within a subnet can communicate directly; devices outside must pass through a router. This means:

- Subnets **contain** broadcast traffic and limit its scope
- Subnets create **natural inspection points** at router boundaries
- Proper subnetting **enforces segmentation** — keeping sensitive systems isolated from general user networks
- Misconfigured subnets can accidentally **expose systems** to unintended traffic

Understanding subnetting is essential for anyone designing, auditing, or defending a network.

---

## Subnetting Reference (CIDR Notation)

| CIDR | Subnet Mask | Hosts per Subnet |
|---|---|---|
| /24 | 255.255.255.0 | 254 |
| /25 | 255.255.255.128 | 126 |
| /26 | 255.255.255.192 | 62 |
| /27 | 255.255.255.224 | 30 |
| /28 | 255.255.255.240 | 14 |
| /29 | 255.255.255.248 | 6 |
| /30 | 255.255.255.252 | 2 |

---

## Exercises Completed
Five full subnetting problems solved, including:
- Identifying network address from host IP + mask
- Calculating broadcast address
- Determining valid host range
- Identifying number of usable hosts
- Determining subnet from CIDR notation

*Screenshots of completed exercises included in original submission.*

---

## Skills Demonstrated
`IPv4 Subnetting` `CIDR Notation` `Subnet Mask Calculation` `Network Boundary Design` `Host Range Analysis`
