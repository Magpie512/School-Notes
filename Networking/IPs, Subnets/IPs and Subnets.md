## IP Addresses (IPv4)
- Format: four octets separated by dots, e.g. `192.168.1.10`
- Each octet = 8 bits, values range from 0–255
- Conceptually split into:
    - **Network portion**: identifies the network
    - **Host portion**: identifies the device within that network
---
## Subnet Masks
- Define how many bits are reserved for the network vs hosts
- Example: `255.255.255.0` = `/24` in CIDR notation
    - 24 bits for network, 8 bits for host
- CIDR notation (`/x`) is shorthand for the number of network bits
---
## Reading IP + Subnet Together
Example: `192.168.1.10/24`
- Network address: `192.168.1.0`
- First usable host: `192.168.1.1`
- Last usable host: `192.168.1.254`
- Broadcast address: `192.168.1.255`
- Total usable hosts: (2^8 - 2 = 254)

Example: `10.0.0.5/16`
- Network address: `10.0.0.0`
- First usable host: `10.0.0.1`
- Last usable host: `10.0.255.254`
- Broadcast address: `10.0.255.255`
- Total usable hosts: (2^{16} - 2 = 65,534)
---
## Quick Techniques
- Hosts per subnet = (2^{\text{host bits}} - 2)
- Block size = (256 - \text{last subnet mask octet})
    - Example: `/26` → mask = 255.255.255.192 → block size = 64
    - Subnets increment by 64 in the last octet: `192.168.1.0`, `192.168.1.64`, `192.168.1.128`, `192.168.1.192`
