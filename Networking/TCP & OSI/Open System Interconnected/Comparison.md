## OSI Model Summary Table

| Layer | Name         | Key Responsibilities                                                                     | Examples                                                               |
| ----- | ------------ | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| **7** | Application  | Provides services directly to end-user applications; defines protocols for communication | HTTP/HTTPS, FTP, SMTP, IMAP, DNS                                       |
| **6** | Presentation | Translates, encrypts, and compresses data; ensures proper format for applications        | SSL/TLS, JPEG, MPEG, ASCII, Unicode, JSON, XML                         |
| **5** | Session      | Establishes, manages, and terminates sessions; synchronization and dialog control        | NetBIOS, RPC, SIP, SMB, PPTP                                           |
| **4** | Transport    | Reliable delivery, segmentation/reassembly, error detection, flow control, multiplexing  | TCP, UDP, SCTP, DCCP                                                   |
| **3** | Network      | Logical addressing, routing, packet forwarding, fragmentation                            | IPv4/IPv6, ICMP, RIP, OSPF, BGP, IPsec                                 |
| **2** | Data Link    | Physical addressing (MAC), framing, error detection, media access control                | Ethernet, Wi-Fi, PPP, HDLC, Switches, Bridges                          |
| **1** | Physical     | Transmission of raw bits over physical medium; defines cables, signals, connectors       | Fiber optics, Ethernet cables, Wi-Fi radio, Bluetooth, Hubs, Repeaters |

---
### How They Work Together
- **Layers 1–2 (Physical & Data Link)**: Handle local delivery and physical transmission.
- **Layer 3 (Network)**: Decides _where_ data goes across networks.
- **Layer 4 (Transport)**: Ensures data arrives reliably and in order.
- **Layer 5–7 (Session, Presentation, Application)**: Manage conversations, format/translate data, and provide user-facing services.