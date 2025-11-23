## What Layer 3 Does
- **Logical addressing**: Assigns IP addresses to devices so they can be uniquely identified on a network.
- **Routing**: Determines the best path for data packets to travel across interconnected networks.
- **Packet forwarding**: Moves packets from source to destination based on logical addressing.
- **Fragmentation & reassembly**: Breaks large packets into smaller ones for transmission and reassembles them at the destination.
---
## Key Responsibilities
- **Path determination**: Chooses the most efficient route for data delivery.
- **Addressing**: Uses IP addresses to identify source and destination devices.
- **Error handling**: Detects and manages issues like unreachable destinations.
- **Traffic control**: Manages congestion and prioritizes certain types of traffic
---
## Examples of Layer 3  Protocols 
| IPv4 / IPv6                             | Logical addressing and packet delivery   |
| --------------------------------------- | ---------------------------------------- |
| ICMP                                    | Error reporting and diagnostics          |
| RIP, OSPF, GBP                          | Routing protocols for path determination |
| IPsec                                   | Provides security at the network layer   |
| ARP - Technically between layer 2 and 3 | Resolves IP addresses to MAC addresses   |
 
---
## Why Layer 3 Matters

- **Scalability**: Enables communication across large, complex networks (like the internet).
- **Inter-networking**: Connects multiple networks together through routers.
- **Reliability**: Ensures packets reach the correct destination, even across multiple hops.
- **Security**: IPsec and similar protocols protect data at this layer.