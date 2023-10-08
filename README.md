# MinecraftNotes
A repo containing various notes on Minecraft server compatibility, among other things

PRs and issues welcome! Feel free to let me know if you've found a workaround, or if the issue has been patched.

## Proxy Compatibility
### Keys
- BungeeForge -> BF
- Proxy Compatible Forge -> PCF
- BungeeGuard -> BG
- ProtocolLib -> PL
- Ambassador -> AMB

| Server Type            | Proxy          | Legacy      | BungeeGuard                | Modern         | Notes |
| ---------------------- | -------------- | ----------- | -------------------------- | -------------- | --- |
| Arclight 1.14.4-1.0.6  | Velocity (AMB) | No          | No (BG v1.2.2, PL v4.5.0)  | N/A (No PCF)   | Generic forwarding error, malformed data |
| Arclight 1.15.2-1.0.19 | Velocity (AMB) | No          | No (BG v1.2.2, PL v5.1.0)  | N/A (No PCF)   | Bad packet when forwarding, test inconclusive |
| Arclight 1.16.5-1.0.24 | Velocity (AMB) | Yes         | Yes (BG v1.2.2, PL v5.1.0) | Yes (With PCF) | |
| Arclight 1.17.1-1.0.2  | Velocity (AMB) | No          | No (BG v1.2.2, PL v5.1.0)  | N/A (No PCF)   | Generic forwarding error, malformed data. Would only start when using Java 16 |
| Arclight 1.18.2-1.0.9  | Velocity (AMB) | No          | No (BG v1.2.2, PL v5.1.0)  | Yes (With PCF) | Generic forwarding error, malformed data |
| Arclight 1.19.2-1.0.2  | Velocity (AMB) | No          | No (BG v1.2.2, PL v5.1.0)  | Yes (With PCF) | Generic forwarding error, malformed data |
| Arclight 1.19.3-1.0.3  | Velocity (AMB) | No          | No (BG v1.2.2, PL v5.1.0)  | Yes (With PCF) | Generic forwarding error, malformed data |
| Arclight 1.19.4-1.0.5  | Velocity (AMB) | No          | No (BG v1.2.2, PL v5.1.0)  | Yes (With PCF 1.19.3) | Generic forwarding error, malformed data |
| Arclight 1.20.1-1.0.1  | Velocity (AMB) | No          | No (BG v1.2.2, PL v5.1.0)  | Yes (With PCF 1.20) | Generic forwarding error, malformed data |
