==### Core Concepts

- **OSI vs TCP/IP Models**
    - OSI: 7 layers (Physical → Application)
    - TCP/IP: 4 layers (Link, Internet, Transport, Application)
    - Useful for mapping protocols and troubleshooting where issues occur.
- **MAC Addresses**
    - Hardware-level identifiers, 48-bit, written in hex (e.g., `00:1A:2B:3C:4D:5E`).
    - Operate at Layer 2 (Data Link).
- **ARP (Address Resolution Protocol)**
    - Maps IP addresses to MAC addresses.
    - Critical for communication inside local networks.

---

### Routing & Switching

- **Default Gateway**
    - The router that connects your local network to others.
- **Static vs Dynamic Routing**
    - Static: manually configured routes.
    - Dynamic: protocols like RIP, OSPF, BGP automatically adjust paths.
- **VLANs (Virtual LANs)**
    - Logical segmentation of networks at Layer 2.
    - Useful for separating traffic (e.g., staff vs guest).

---

### Addressing & Services

- **DHCP (Dynamic Host Configuration Protocol)**
    - Automatically assigns IPs, subnet masks, gateways, DNS.
- **DNS (Domain Name System)**
    - Translates human-readable names (`example.com`) into IP addresses.
- **NAT (Network Address Translation)**
    - Allows multiple devices to share one public IP.
    - Essential for IPv4 address conservation.

---

### Security & Management

- **Firewalls**
    - Control traffic based on rules (ports, IPs, protocols).
- **ACLs (Access Control Lists)**
    - Rules applied to routers/switches to permit/deny traffic.
- **VPNs (Virtual Private Networks)**
    - Secure tunnels across public networks.
- **SNMP (Simple Network Management Protocol)**
    - Used for monitoring and managing devices.

---

### Practical Tools

- **Ping / Traceroute**
    - Basic connectivity and path testing.
- **Netstat / Wireshark**
    - Netstat: shows active connections.
    - Wireshark: packet capture and analysis.
- **CLI Commands (Cisco IOS)**
    - `show ip route`, `show running-config`, `interface range`, etc.

---

### Modern Topics

- **IPv6 Adoption**
    - Dual-stack environments (IPv4 + IPv6).
- **QoS (Quality of Service)**
    - Prioritizing traffic (e.g., VoIP vs bulk downloads).
- **SDN (Software Defined Networking)**
    - Centralized control, programmable networks.
- **Cloud Networking**
    - Virtual networks, load balancers, firewalls in cloud platforms.

---

If you’re building notes for teaching, I’d suggest mapping these into **three tiers**:

1. **Foundations** (IP, subnetting, OSI/TCP-IP)
2. **Operations** (routing, VLANs, DHCP/DNS/NAT)
3. **Security & Modern Trends** (firewalls, VPNs, IPv6, SDN, cloud)

Would you like me to scaffold this into a **modular cheat sheet format** (like a one-page quick reference) that you could hand out in your club sessions?