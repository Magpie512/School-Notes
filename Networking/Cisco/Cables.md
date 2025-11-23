### Common Cisco Cable Types
- **Straight-Through Ethernet Cable**
    - Connects different devices (e.g., PC → Switch, Switch → Router).
    - Uses **T568A to T568B wiring**.
    - Standard for most LAN connections.
- **Crossover Ethernet Cable**
    - Connects similar devices (e.g., Switch → Switch, PC → PC).
    - Uses **T568B to T568B with crossed pairs**.
    - Largely replaced by **Auto-MDI/MDIX** in modern Cisco gear.
- **Rollover (Console) Cable**
    - Flat cable with reversed pinouts.
    - Connects a PC’s serial port to a Cisco device’s **console port** for configuration.
- **Fiber-Optic Cable**
    - Used for high-speed, long-distance connections (e.g., backbone links).
    - Types: **Single-mode (SMF)** for long distances, **Multi-mode (MMF)** for shorter runs.
- **Serial DCE/DTE Cable**
    - Connects routers via WAN interfaces in labs or legacy setups.
    - Provides clocking (DCE side) for synchronization.

---
### Ethernet Cable Categories (Cat3 → Cat8)
- **Cat5e / Cat6**: Most common in Cisco LANs, supporting up to 1–10 Gbps.
- **Cat7 / Cat8**: Used in data centers for higher bandwidth and shielding.
---
### Cisco-Specific Connectors
- **RJ-45**: Standard for Ethernet ports (10/100/1000 Mbps).
- **SFP / SFP+ Modules**: For fiber or copper uplinks.
- **XENPAK / QSFP**: High-speed fiber modules for enterprise switches.
---
### Quick Reference Table

|Cable Type|Use Case|Connector|
|---|---|---|
|Straight-Through|PC → Switch, Switch → Router|RJ-45|
|Crossover|Switch → Switch, PC → PC|RJ-45|
|Rollover (Console)|PC → Cisco Console Port|DB9 / RJ-45|
|Fiber-Optic (SMF/MMF)|High-speed backbone, long runs|LC/SC/SFP|
|Serial DCE/DTE|Router → Router (WAN labs)|Serial|

---
**In practice:** For modern Cisco labs (like Packet Tracer or real hardware), you’ll mostly use **straight-through Ethernet cables** for connections, **console cables** for device setup, and **fiber cables** for high-speed uplinks.