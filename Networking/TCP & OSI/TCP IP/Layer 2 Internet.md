## TCP/IP Layer 2 — Internet Layer
- **Purpose**: Handles logical addressing and routing of packets across networks.
- **Core function**: Decides _where_ data should go and _how_ to get there.
- **Packet delivery**: Encapsulates data into packets and ensures they reach the correct destination.
- **Inter-networking**: Connects multiple networks together, enabling global communication (the foundation of the internet).
---
## Key Responsibilities
- **Logical addressing**: Uses IP addresses to identify source and destination devices.
- **Routing**: Determines the best path for packets to travel across networks.
- **Fragmentation & reassembly**: Splits large packets into smaller ones for transmission and reassembles them at the destination.
- **Error handling**: Reports issues like unreachable destinations.
---
## Examples of Internet Layer Protocols

|Protocol|Purpose|
|---|---|
|IPv4 / IPv6|Logical addressing and packet delivery|
|ICMP|Error reporting and diagnostics (e.g., ping)|
|ARP|Resolves IP addresses to MAC addresses (operates between Link & Internet layers)|
|RIP, OSPF, BGP|Routing protocols for path determination|
|IPsec|Provides security at the network layer|

---
## Why the Internet Layer Matters
- **Scalability**: Enables communication across massive, interconnected networks (like the global internet).
- **Reliability**: Ensures packets reach the correct destination, even across multiple hops.
- **Inter-networking**: Allows different types of networks (LANs, WANs) to connect seamlessly.
- **Security**: Protocols like IPsec protect data at this layer.