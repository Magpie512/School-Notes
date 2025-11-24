### Console Line Commands

- **`line console 0`** → Enter console line configuration mode.
- **`password [pass]`** → Set console password.
- **`login`** → Require password login on the console.
- **`login local`** → Use local user database for console authentication.
- **`exec-timeout [minutes] [seconds]`** → Disconnect idle console sessions (e.g., `exec-timeout 5 0`).
- **`absolute-timeout [minutes]`** → Force console session termination after a fixed time, regardless of activity.
- **`session-timeout [minutes]`** → Limit maximum duration of a console session (used with AAA/TACACS+).
- **`logging synchronous`** → Prevent system messages from interrupting console input.
- **`no exec`** → Disable EXEC mode on the console line (rarely used, prevents interactive sessions).
---
### VTY Line Commands (Remote Access)

- **`line vty 0 4`** → Enter VTY line configuration mode (supports up to 5 simultaneous remote sessions).
- **`line vty 0 15`** → Configure up to 16 VTY lines (common on newer IOS versions).
- **`password [pass]`** → Set VTY line password (used if `login` is configured).
- **`login`** → Require password login on VTY lines.
- **`login local`** → Use local user database for authentication.
- **`transport input ssh`** → Allow only SSH connections (recommended).
- **`transport input telnet ssh`** → Allow both Telnet and SSH (not recommended).
- **`transport output [protocols]`** → Control which protocols can be initiated from the VTY session.
- **`exec-timeout [minutes] [seconds]`** → Disconnect idle remote sessions.
- **`absolute-timeout [minutes]`** → Force remote session termination after a fixed time.
- **`session-timeout [minutes]`** → Limit maximum duration of a VTY session (used with AAA/TACACS+).
- **`access-class [ACL-number] in`** → Apply an ACL to restrict which IPs can connect to VTY lines.
- **`exec` / `no exec`** → Enable or disable EXEC mode on VTY lines.
---
### Security Best Practices for Console & VTY

- Always use **`login local`** with **user accounts** (`username [name] privilege 15 secret [pass]`) instead of simple line passwords.
- Restrict remote access to **SSH only** (`transport input ssh`).
- Apply **ACLs** with `access-class` to limit which IPs can connect remotely.
- Configure **timeouts** (`exec-timeout`, `absolute-timeout`, `session-timeout`) to prevent abandoned sessions.
- Use **`logging synchronous`** on the console for readability.
- Disable unused VTY lines or use `no exec` if remote access is not required.
---
### Example Secure Setup Workflow

```bash
Router> enable
Router# configure terminal
Router(config)# line console 0
Router(config-line)# password Ciscoconpa55
Router(config-line)# login local
Router(config-line)# exec-timeout 5 0
Router(config-line)# logging synchronous
Router(config-line)# exit

Router(config)# line vty 0 4
Router(config-line)# login local
Router(config-line)# transport input ssh
Router(config-line)# exec-timeout 5 0
Router(config-line)# access-class 10 in
Router(config-line)# exit
```