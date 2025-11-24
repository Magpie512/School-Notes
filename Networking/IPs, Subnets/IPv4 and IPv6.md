**IPv4 uses 32-bit addresses (like `192.168.1.1`) while IPv6 uses 128-bit addresses (like `2001:0db8:85a3::8a2e:0370:7334`). The main difference is that IPv6 provides an almost unlimited number of addresses and includes built-in features for security and efficiency, whereas IPv4 is limited to about 4.3 billion addresses and requires workarounds.**

---
## How to Read IPv4
- **Format:** Four decimal numbers separated by dots, e.g. `192.168.0.1`
- **Range:** Each number (octet) is 0–255
- **Subnet masks:** Define network vs host portion, e.g. `/24` means 24 bits for network
- **Example:**
    - `192.168.1.10/24` → Network: `192.168.1.0`, Broadcast: `192.168.1.255`, Hosts: 254 usable
---
## How to Read IPv6
- **Format:** Eight groups of four hexadecimal digits separated by colons, e.g. `2001:0db8:85a3:0000:0000:8a2e:0370:7334`
- **Compression rules:**
    - Leading zeros can be omitted (`0db8` → `db8`)
    - Consecutive groups of zeros can be replaced with `::` (only once per address)
- **Example:**
    - `2001:db8::1` is shorthand for `2001:0db8:0000:0000:0000:0000:0000:0001`
---
## Key Differences in Uses

|Feature|IPv4|IPv6|
|---|---|---|
|Address size|32-bit (~4.3 billion addresses)|128-bit (~340 undecillion addresses)|
|Format|Dotted decimal (`192.168.1.1`)|Hexadecimal with colons (`2001:db8::1`)|
|Security|No built-in encryption (requires IPsec as add-on)|IPsec built-in|
|Configuration|Manual or DHCP|Auto-configuration supported|
|Routing|Larger, complex headers|Simplified headers for efficiency|
|QoS (Quality of Service)|Limited support|Better support for prioritizing traffic|

---
## Why It Matters
- **IPv4** is still dominant and widely supported, but addresses are nearly exhausted.
- **IPv6** was designed to handle the explosion of internet-connected devices (IoT, mobile, cloud).
- IPv6 also improves **security**, **performance**, and **scalability** for modern networks.