
## TCP/IP Layer 3 — Transport Layer
- **Purpose**: Provides end-to-end communication between applications on different devices.
- **Connection management**: Establishes, maintains, and terminates logical connections.
- **Reliability vs. speed**: Offers both reliable (TCP) and fast but connectionless (UDP) delivery.
- **Segmentation & reassembly**: Breaks large messages into smaller segments and reassembles them at the destination.
- **Multiplexing**: Uses port numbers to allow multiple applications to share the same network connection.

---
### Key Responsibilities
- **Error detection & correction**: Ensures data arrives intact.
- **Flow control**: Prevents fast senders from overwhelming slower receivers.
- **Congestion control**: Adjusts transmission speed to avoid network overload.
- **End-to-end delivery**: Guarantees communication between processes, not just devices.

---
## Examples of Transport Layer Protocols

|Protocol|Purpose|
|---|---|
|**TCP (Transmission Control Protocol)**|Reliable, ordered, connection-oriented communication (web, email, file transfer)|
|**UDP (User Datagram Protocol)**|Fast, connectionless communication (streaming, gaming, VoIP)|
|**SCTP (Stream Control Transmission Protocol)**|Advanced reliability with multi-streaming|
|**DCCP (Datagram Congestion Control Protocol)**|Congestion-controlled transport for streaming media|

---

## Why the Transport Layer Matters

- **Reliability**: Ensures data arrives intact and in the correct order, critical for things like banking, file transfers, and secure communication.
- **Efficiency**: Flow and congestion control prevent network overload, keeping performance smooth.
- **Flexibility**: Applications can choose between TCP (reliable) and UDP (fast) depending on their needs (e.g., video calls vs. file downloads).
- **User experience**: Smooth browsing, responsive gaming, uninterrupted streaming, and error-free communication all depend on this layer.
- **Foundation for applications**: Without Transport Layer services, higher-level protocols (like HTTP, SMTP, or DNS) couldn’t function properly.