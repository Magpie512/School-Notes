### IP Address Identification & Local vs Public

**Private (Local) IP Ranges**  
These are reserved for internal networks and are **not routable on the public internet**:

- **Class A:** `10.0.0.0 – 10.255.255.255`
- **Class B:** `172.16.0.0 – 172.31.255.255`
- **Class C:** `192.168.0.0 – 192.168.255.255`

**Loopback & Special Addresses**

- **`127.0.0.0/8`** → Loopback range (commonly `127.0.0.1` = localhost).
- **`169.254.0.0/16`** → APIPA (Automatic Private IP Addressing, used when DHCP fails).
- **`0.0.0.0`** → Default route / “unspecified” address.
- **`255.255.255.255`** → Broadcast to all hosts on the local network.

**Public IPs**

- Any IP **outside the private ranges** is considered public and routable on the internet.
- Example: `8.8.8.8` (Google DNS) is a public IP.

**How to Tell if an IP is Local**

1. **Check the range:**
    - If it falls into `10.x.x.x`, `172.16–31.x.x`, or `192.168.x.x`, it’s private/local.
2. **Check special cases:**
    - `127.x.x.x` → loopback (local to the device itself).
    - `169.254.x.x` → APIPA (local fallback, not internet-routable).
3. **Otherwise:** It’s a public IP.

**IPv6 Local vs Global**

- **Link-local:** `fe80::/10` → Used for communication on the same link, auto-assigned.
- **Unique local:** `fc00::/7` → Private IPv6 addresses (like IPv4 private ranges).
- **Global unicast:** `2000::/3` → Publicly routable IPv6 addresses.

**Useful Commands**

- **`ping [IP]`** → Test connectivity.
- **`traceroute [IP]`** → See if traffic leaves the local network.
- **`show ip interface brief`** → Verify assigned IPs on Cisco devices.
- **`ipconfig` / `ifconfig`** → Check IP assignment on PCs.

---

### Quick Reference

- **Local (private):** 10.x.x.x, 172.16–31.x.x, 192.168.x.x
- **Loopback:** 127.x.x.x
- **APIPA:** 169.254.x.x
- **Public:** Anything else (globally routable)
- **IPv6 local:** fe80::/10 (link-local), fc00::/7 (unique local)