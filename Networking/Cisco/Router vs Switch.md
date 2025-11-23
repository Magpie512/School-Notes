### Cisco Router vs Switch Commands

| Category                    | Router Commands                                                                                        | Switch Commands                                                                    | Notes                                                                    |
| --------------------------- | ------------------------------------------------------------------------------------------------------ | ---------------------------------------------------------------------------------- | ------------------------------------------------------------------------ |
| **Mode Navigation**         | `enable`, `configure terminal`, `exit`                                                                 | `enable`, `configure terminal`, `exit`                                             | Same across both devices.                                                |
| **Basic Setup**             | `hostname Router1`, `banner motd #message#`                                                            | `hostname Switch1`, `banner motd #message#`                                        | Identical for naming and login banners.                                  |
| **Interface Configuration** | `interface gig0/0`  <br>`ip address 192.168.1.1 255.255.255.0`  <br>`no shutdown`                      | `interface fast0/1`  <br>`switchport mode access`  <br>`switchport access vlan 10` | Routers configure IP addresses; switches configure VLANs and port modes. |
| **IP Services**             | `ip route 0.0.0.0 0.0.0.0 [next-hop]`  <br>`router ospf 1`  <br>`network 192.168.1.0 0.0.0.255 area 0` | `ip default-gateway 192.168.1.1`                                                   | Routers handle routing protocols; switches only set a default gateway.   |
| **Verification**            | `show ip route`  <br>`show running-config`  <br>`ping [IP]`  <br>`traceroute [IP]`                     | `show vlan brief`  <br>`show mac address-table`  <br>`show running-config`         | Routers verify routes; switches verify VLANs and MAC tables.             |
| **Saving Config**           | `copy running-config startup-config`                                                                   | `copy running-config startup-config`                                               | Same across both devices.                                                |
| **Troubleshooting**         | `debug ip packet`  <br>`show ip interface brief`                                                       | `show interfaces status`  <br>`show spanning-tree`                                 | Routers focus on IP connectivity; switches focus on port/VLAN status.    |

---
### Key Differences
- **Routers**: Focus on **Layer 3 (Network Layer)** tasks, IP addressing, routing, WAN connectivity.
- **Switches**: Focus on **Layer 2 (Data Link Layer)** tasks, VLANs, MAC address tables, port configurations.
- **Overlap**: Both share core navigation, setup, and saving commands.