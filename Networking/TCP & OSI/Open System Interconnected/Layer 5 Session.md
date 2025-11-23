## What Layer 5 Does
- **Manages sessions**: Establishes, maintains, and terminates communication sessions between applications.
- **Synchronization**: Keeps track of dialog control, ensuring that data streams remain organized and synchronized.
- **Checkpointing & recovery**: Allows sessions to resume from a known point if interrupted.
- **Dialog control**: Determines whether communication is half-duplex (one direction at a time) or full-duplex (both directions simultaneously).
---
## Key Responsibilities
- **Session establishment**: Initiates communication between two devices or applications.
- **Session maintenance**: Keeps the connection alive and manages data exchange.
- **Session termination**: Ends the communication cleanly when tasks are complete.
- **Synchronization points**: Inserts checkpoints so large data transfers can restart from the last checkpoint if a failure occurs.
---
## Examples of Layer 5 Functions

| Protocol                                 | Purpose                                                         |
| ---------------------------------------- | --------------------------------------------------------------- |
| NetBIOS                                  | Provides session services for Windows-based networks            |
| RPC (Remote Procedure Call)              | Allows programs to execute procedures on remote systems         |
| PPTP (Point-to-Point Tunneling Protocol) | Supports VPN tunnelinIg sessions                                |
| SIP (Session Initiation Protocol)        | Establishes and manages multimedia sessions (VoIP, video calls) |
| SMB (Server Messages Block)              | Manages sessions for file and printer sharing                   |

---
## Why Layer 5 Matters

- **Reliability**: Ensures that communication sessions don’t drop unexpectedly.
- **Efficiency**: Manages dialog flow so resources aren’t wasted.
- **Resilience**: Checkpointing allows recovery from crashes or interruptions.
- **User experience**: Smooth session handling means uninterrupted video calls, file transfers, and remote logins