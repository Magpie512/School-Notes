## What Layer 2 Does
- **Physical addressing**: Uses MAC (Media Access Control) addresses to identify devices on the same local network.
- **Error detection & correction**: Ensures data frames are transmitted without corruption.
- **Framing**: Packages raw bits from the physical layer into structured units called _frames_.
- **Flow control**: Manages the rate of data transmission between devices.
- **Media access control**: Determines how devices share access to the physical medium (e.g., Ethernet, Wi-Fi).
---
## Key Responsibilities
- **Reliable local delivery**: Ensures data is delivered across a single link or local network segment.
- **MAC addressing**: Provides unique identifiers for devices within a LAN.
- **Error handling**: Uses checksums (CRC) to detect corrupted frames.
- **Access control**: Prevents collisions and manages how multiple devices use the same medium.
---
## Examples of Layer 2 Protocols

| Protocols                           | Purpose                                                                  |
| ----------------------------------- | ------------------------------------------------------------------------ |
| Ethernet (IEEE 802.3)               | Wired LAN Communication                                                  |
| Wi-Fi (IEEE 802.11)                 | Wireless LAN Communication                                               |
| PPP (Point-to-Point Protocol)       | Direct connections between two nodes                                     |
| HDLC (High-Level Data Link Control) | Reliable point-to-point communication                                    |
| ARP (Address Resolution Protocol)   | Resolves IP addresses to MAC addresses (*operates between Layer 2 & 3)   |
| Switches & Bridges                  | Devices that operate at Layer 2 to forward frames based on MAC addresses |

---
## Why Layer 2 Matters

- **Local communication**: Enables devices on the same network segment to talk to each other.
- **Efficiency**: Reduces errors and collisions in data transmission.
- **Foundation for higher layers**: Provides the structure (frames, MAC addresses) that Layer 3 (Network Layer) builds on.
- **Security**: VLANs and MAC filtering help control access at this layer.