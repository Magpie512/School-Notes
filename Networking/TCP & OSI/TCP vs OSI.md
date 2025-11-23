## OSI vs TCP/IP Layer Mapping

|OSI Model (7 Layers)|TCP/IP Model (4 Layers)|Key Notes|
|---|---|---|
|**7 – Application**|**4 – Application**|TCP/IP merges OSI’s Application, Presentation, and Session layers into one.|
|**6 – Presentation**|**4 – Application**|Formatting, encryption, compression handled here in TCP/IP.|
|**5 – Session**|**4 – Application**|Session management also part of TCP/IP’s Application layer.|
|**4 – Transport**|**3 – Transport**|End-to-end communication, reliability, flow control (TCP, UDP).|
|**3 – Network**|**2 – Internet**|Logical addressing, routing, packet forwarding (IP, ICMP, ARP).|
|**2 – Data Link**|**1 – Network Access (Link)**|Framing, MAC addressing, error detection, local delivery.|
|**1 – Physical**|**1 – Network Access (Link)**|Defines cables, signals, connectors, and transmission media.|

---
## Key Differences

- **OSI is conceptual**: 7 layers, used mainly for teaching and theoretical design.
- **TCP/IP is practical**: 4 layers, the actual framework the internet runs on.
- **Top layers collapsed**: TCP/IP’s Application layer combines OSI’s top three (Application, Presentation, Session).
- **Bottom layers merged**: TCP/IP’s Network Access layer combines OSI’s Physical and Data Link layers.