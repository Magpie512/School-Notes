## What Layer 4 Does
- **Reliable delivery of data**: Ensures that information is transferred completely and correctly between devices.
- **Segmentation & reassembly**: Breaks large messages into smaller chunks (segments) and reassembles them at the destination.
- **Error detection & correction**: Uses checksums and acknowledgments to confirm data integrity.
- **Flow control**: Prevents fast senders from overwhelming slower receivers.
- **Connection management**: Establishes, maintains, and terminates logical connections between applications.
---
## Key Responsibilities
- **Multiplexing**: Allows multiple applications to share the same network connection by assigning port numbers.
- **Reliable vs. unreliable transport**: Supports both guaranteed delivery (TCP) and faster, connectionless delivery (UDP).
- **Error handling**: Detects lost or corrupted segments and retransmits them.
- **End-to-end communication**: Provides direct communication between processes on different devices
---
## Examples of Layer 4 Protocols
| Protocol                                    | Purpose                                                                 |
| ------------------------------------------- | ----------------------------------------------------------------------- |
| TCP (Transmission Control Protocol)         | Reliable, connection-oriented communication (e.g., web browsing, email) |
| UDP (User Datagram Protocol)                | Fast, connectionless communication (e.g., streaming, gaming)            |
| SCTP (Stream Control Transmission Protocol) | Supports multi-streaming and multi-homing for advanced reliability      |
| DCCP (Datagram Congestion Control Protocol) | Provides congestion-controlled transport for streaming media            |

---
## Why Layer 4 Matters

- **Reliability**: Ensures data arrives intact and in the right order.
- **Efficiency**: Flow control and congestion management optimize network performance.
- **Flexibility**: Supports both reliable (TCP) and fast (UDP) communication depending on application needs.
- **User experience**: Smooth video calls, responsive gaming, and error-free file transfers all depend on this layer