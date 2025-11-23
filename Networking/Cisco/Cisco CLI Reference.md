### Navigation & Modes
- **`enable`** → Enter privileged EXEC mode (from user mode).
- **`disable`** → Return to user EXEC mode.
- **`configure terminal`** → Enter global configuration mode.
- **`exit`** → Move back one level in the CLI hierarchy.
---
### Device Setup
- **`hostname [name]`** → Set the device’s hostname.
- **`banner motd #message#`** → Configure a login message.
- **`clock set HH:MM:SS MONTH DAY YEAR`** → Set the system clock.
- **`line console 0`** → Configure console line.
- **`password [pass]`** → Set console password.
- **`login`** → Require password login.
- **`enable secret [pass]`** → Set encrypted privileged EXEC password.
- **`service password-encryption`** → Encrypt all plaintext passwords in config.
---
### Interface Configuration
- **`interface [type/number]`** → Enter interface configuration mode (e.g., `interface gig0/0`).
- **`ip address [IP] [subnet]`** → Assign IP address to the interface.
- **`no shutdown`** → Enable the interface (interfaces are disabled by default).
---
### Bulk Configuration & Macros
- **`interface range [type/port - port]`** → Configure multiple interfaces at once.
- **`interface range [type/port, type/port]`** → Configure non-contiguous interfaces.
- **`define interface-range [name] [ports]`** → Create a reusable macro.
---
### VLAN & Switching
- **`vlan [id]`** → Create VLAN.
- **`name [vlan-name]`** → Assign VLAN name.
- **`switchport mode access`** → Set port to access mode.
- **`switchport access vlan [id]`** → Assign VLAN to access port.
- **`switchport mode trunk`** → Configure trunk mode.
- **`switchport trunk allowed vlan [list]`** → Allow specific VLANs on trunk.
- **`show vlan brief`** → Verify VLANs and port assignments.
- **`show interfaces trunk`** → Verify trunk configuration.
---
### Routing (Static & Dynamic)
- **`ip route [dest-network] [mask] [next-hop]`** → Configure static route.
- **`router rip`** → Enable RIP routing protocol.
- **`version 2`** → Use RIP v2.
- **`network [network-id]`** → Advertise network in RIP.
- **`router ospf [process-id]`** → Enable OSPF.
- **`network [network] [wildcard] area [id]`** → Define OSPF area.
- **`router eigrp [AS]`** → Enable EIGRP.
- **`network [network-id]`** → Advertise network in EIGRP.
- **`show ip route`** → View routing table.
- **`show ip protocols`** → Verify routing protocols.
---
### Security & Access Control
- **`access-list [number] permit/deny [protocol] [src] [wildcard] [dest] [wildcard]`** → Create ACL.
- **`ip access-group [number] in/out`** → Apply ACL to interface.
- **`show access-lists`** → Verify ACLs.
- **`login block-for [seconds] attempts [count] within [seconds]`** → Configure login security.
- **`username [name] secret [pass]`** → Create local user with encrypted password.
---
### NAT & DHCP
- **`ip nat inside`** → Mark interface as inside NAT.
- **`ip nat outside`** → Mark interface as outside NAT.
- **`ip nat inside source static [local-ip] [global-ip]`** → Configure static NAT.
- **`ip nat inside source list [ACL] interface [outside-if] overload`** → Configure PAT (NAT overload).
- **`show ip nat translations`** → Verify NAT.
- **`ip dhcp pool [name]`** → Create DHCP pool.
- **`network [network] [mask]`** → Define DHCP network.
- **`default-router [IP]`** → Set default gateway for DHCP clients.
- **`dns-server [IP]`** → Set DNS server for DHCP clients.
- **`show ip dhcp binding`** → Verify DHCP leases.
---
### Verification & Troubleshooting
- **`show running-config`** → View current configuration.
- **`show startup-config`** → View saved configuration.
- **`show ip interface brief`** → Quick summary of interfaces, IPs, and status.
- **`ping [IP]`** → Test connectivity.
- **`traceroute [IP]`** → Trace the path packets take.
- **`show version`** → View IOS version, uptime, hardware info.
- **`show interfaces`** → Detailed interface stats.
- **`show cdp neighbors`** → Discover directly connected Cisco devices.
- **`show arp`** → View ARP table.
- **`debug ip packet`** → Debug IP packets (use carefully).
- **`terminal monitor`** → Display log messages on console.
- **`logging [IP]`** → Send logs to syslog server.
---
### Saving & Reloading
- **`copy running-config startup-config`** → Save current config to NVRAM.
- **`write memory`** → Save config (same as `copy run start`).
- **`erase startup-config`** → Clear saved config.
- **`delete vlan.dat`** → Reset VLAN database.
- **`reload`** → Restart the device.
- **`reload in [minutes]`** → Schedule reload.
- **`boot system [file]`** → Specify IOS image to boot.
---
### Wireless (if applicable)
- **`dot11 ssid [name]`** → Create SSID.
- **`authentication open`** → Configure open authentication.
- **`guest-mode`** → Enable SSID broadcast.
- **`interface dot11radio 0`** → Configure wireless interface.
---
### Example Workflow
1. Enter privileged mode:
    
    ```bash
    Router> enable
    ```
    
2. Enter global config:
    
    ```bash
    Router# configure terminal
    ```
    
3. Configure an interface:
    
    ```bash
    Router(config)# interface gig0/0
    Router(config-if)# ip address 192.168.1.1 255.255.255.0
    Router(config-if)# no shutdown
    ```
    
4. Verify:
    
    ```bash
    Router# show ip interface brief
    ```
    
---
### Why These Commands Matter
- **Foundation for CCNA/CCNP labs**: These are the building blocks for Cisco certifications.
- **Real-world troubleshooting**: Commands like `ping`, `show running-config`, and `traceroute` are essential for diagnosing network issues.
- **Device management**: Without commands like `copy running-config startup-config`, changes would be lost after a reboot.
- **Scalable configuration**: `interface range` and macros let you configure dozens of ports in seconds,  perfect for classroom labs, club demos, and real-world switch setups.
- **Advanced scenarios**: Routing protocols, ACLs, NAT, and DHCP are critical for simulating enterprise networks and preparing for certification exams.

