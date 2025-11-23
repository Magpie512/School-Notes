## TCP/IP Layer 1 — Network Access (Link) Layer
- **Lowest layer in TCP/IP**: Deals with how data is physically transmitted across the network medium.
- **Encapsulation**: Packages IP packets into frames for transmission over physical hardware.
- **Hardware interaction**: Defines how devices like switches, routers, and NICs (network interface cards) communicate.
- **Media access control**: Determines how devices share access to the physical medium (wired or wireless).

---
## Key Responsibilities
- **Framing**: Structures raw bits into frames for transmission.
- **Physical addressing**: Uses MAC addresses to identify devices on a local network.
- **Error detection**: Ensures frames aren’t corrupted during transmission (via CRC checks).
- **Access control**: Manages how multiple devices use the same medium without collisions.
- **Medium specification**: Defines cables, connectors, frequencies, and signaling methods.

---
## Examples of Link Layer Protocols & Technologies

|Protocol/Technology|Purpose|
|---|---|
|Ethernet (IEEE 802.3)|Wired LAN communication|
|Wi-Fi (IEEE 802.11)|Wireless LAN communication|
|PPP (Point-to-Point Protocol)|Direct connections between two nodes|
|ARP|Resolves IP addresses to MAC addresses (operates between Internet & Link layers)|
|Switches & Bridges|Forward frames based on MAC addresses|
|DSL, Fiber, Coaxial|Physical transmission mediums|

---
## Why the Link Layer Matters

- **Foundation of networking**: Without this layer, higher layers couldn’t send or receive data.
- **Local communication**: Enables devices on the same network segment to talk to each other.
- **Efficiency**: Reduces errors and collisions in data transmission.
- **Compatibility**: Ensures different hardware and media types can interoperate.
