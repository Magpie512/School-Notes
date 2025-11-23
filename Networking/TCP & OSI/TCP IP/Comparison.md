## TCP/IP Model Summary

|Layer (Numbered)|Name|Key Responsibilities|Examples|
|---|---|---|---|
|**4 (Highest)**|Application|Provides services directly to user applications; handles data formatting, encryption, and communication|HTTP/HTTPS, FTP, SMTP, IMAP/POP3, DNS, SSH|
|**3**|Transport|End-to-end communication; segmentation/reassembly; error detection; flow & congestion control; multiplexing via ports|TCP, UDP, SCTP, DCCP|
|**2**|Internet|Logical addressing and routing; packet forwarding; fragmentation/reassembly; error reporting|IPv4, IPv6, ICMP, ARP, RIP, OSPF, BGP, IPsec|
|**1 (Lowest)**|Network Access (Link)|Physical addressing (MAC); framing; error detection; media access control; defines hardware transmission|Ethernet, Wi-Fi, PPP, DSL, Fiber, Switches, Bridges|

---

## How They Work Together

- **Layer 1 (Link)**: Defines how bits move across physical media (cables, Wi-Fi, etc.).
- **Layer 2 (Internet)**: Decides _where_ packets go and _how_ they get there.
- **Layer 3 (Transport)**: Ensures data arrives reliably and in the right order.
- **Layer 4 (Application)**: Provides the actual services users interact with (web, email, file transfer).