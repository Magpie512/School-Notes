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
- **`ip helper-address [IP]`** → Forward DHCP requests to a remote server.
- **`ip default-gateway [IP]`** → Set default gateway (used on switches without routing enabled).
- **`ip address dhcp`** → Configure interface to obtain IP via DHCP.
- **`ipv6 address [address/prefix]`** → Assign IPv6 address to interface.
- **`ipv6 unicast-routing`** → Enable IPv6 routing globally.
- **`show ipv6 interface brief`** → Verify IPv6 addresses and interface status.
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
- **`spanning-tree vlan [id] priority [value]`** → Set STP priority for root bridge election.
- **`spanning-tree portfast`** → Enable fast transition to forwarding state (for end devices).
- **`spanning-tree bpduguard enable`** → Disable port if BPDU received (protects against rogue switches).
- **`show spanning-tree`** → Verify STP status.
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
## **Login Security**
- **`login block-for [seconds] attempts [count] within [seconds]`** → Configure brute force protection (e.g., `login block-for 180 attempts 4 within 120`).
- **`login delay [seconds]`** → Introduce delay after failed login attempts.
- **`login on-failure log`** → Log failed login attempts.
- **`login on-success log`** → Log successful login attempts.
## **User Accounts & Passwords**
- **`username [name] secret [pass]`** → Create local user with encrypted password.
- **`username [name] privilege [level] secret [pass]`** → Create local user with privilege level (0–15).
- **`enable secret [pass]`** → Set encrypted privileged EXEC password.
- **`security passwords min-length [value]`** → Enforce minimum password length (e.g., `security passwords min-length 10`).
- **`password aging [days]`** → Force password expiration after a set number of days.
- **`password encryption aes`** → Use AES encryption for stored passwords (stronger than the default).
## **Line Configuration**
- **`line console 0`** → Enter console line configuration mode.
    - **`password [pass]`** → Set console password.
    - **`login`** → Require password login.
    - **`exec-timeout [minutes] [seconds]`** → Disconnect idle console sessions (e.g., `exec-timeout 5 0`).
- **`line vty 0 4`** → Enter VTY line configuration mode (remote access).
    - **`transport input ssh`** → Allow only SSH connections.
    - **`login local`** → Use local user database for authentication.
    - **`exec-timeout [minutes] [seconds]`** → Disconnect idle remote sessions.
## **SSH Configuration**
- **`ip domain-name [name]`** → Set device domain name (required for RSA key generation).
- **`crypto key generate rsa modulus [bits]`** → Generate RSA keys for SSH (e.g., 1024 or 2048 bits).
- **`ip ssh version 2`** → Enforce SSH v2 for secure remote access.
### **Additional Hardening**
- **`no cdp run`** → Disable CDP globally (reduce information leakage).
- **`no ip source-route`** → Prevent source-routed packets.
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
- **`logging buffered [size]`** → Store logs in memory buffer.
- **`logging host [IP]`** → Send logs to external syslog server.
- **`debug [protocol]`** → Debug specific protocol.
- **`undebug all`** → Stop all debugging.
- **`show logging`** → View log messages.
---
### Saving & Reloading
- **`copy running-config startup-config`** → Save current config to NVRAM.
- **`write memory`** → Save config (same as `copy run start`).
- **`erase startup-config`** → Clear saved config.
- **`delete vlan.dat`** → Reset VLAN database.
- **`reload`** → Restart the device.
- **`reload in [minutes]`** → Schedule reload.
- **`boot system [file]`** → Specify IOS image to boot.
- **`copy tftp running-config`** → Load config from TFTP server.
- **`copy running-config tftp`** → Save config to TFTP server.
- **`copy flash:[file] tftp`** → Backup IOS image.
- **`show flash`** → Verify files in flash memory.
---
### Wireless (if applicable)

- **`dot11 ssid [name]`** → Create SSID.
- **`authentication open`** → Configure open authentication.
- **`guest-mode`** → Enable SSID broadcast.
- **`interface dot11radio 0`** → Configure wireless interface.
---
### Service Control & Environment
- **`no ip domain-lookup`** → Disable DNS lookups on mistyped commands (prevents CLI delays).
- **`no logging console`** → Stop system messages from interrupting console input.
- **`ip domain-name [name]`** → Set device domain name (often required for crypto key generation).
- **`no ip http server`** → Disable the built-in HTTP server (security hardening).
- **`service password-encryption`** → Encrypt plaintext passwords in configuration (basic obfuscation).
---
### QoS & Traffic Management
- **`mls qos`** → Enable QoS globally.
- **`priority-queue out`** → Configure priority queue for outbound traffic.
- **`class-map [name]`** → Define traffic classification.
- **`policy-map [name]`** → Define QoS policies.
- **`service-policy output [policy]`** → Apply QoS policy to interface.