# MinecraftNotes
A repo containing various notes on Minecraft server compatibility, among other things

PRs and issues welcome! Feel free to let me know if you've found a workaround, or if the issue has been patched.

## Proxy Compatibility
### Keys
- [BungeeForge](https://github.com/caunt/BungeeForge) -> BF
- [Proxy Compatible Forge](https://github.com/adde0109/Proxy-Compatible-Forge) -> PCF
- [BungeeGuard](https://github.com/lucko/BungeeGuard) -> BG
- [ProtocolLib](https://github.com/dmulloy2/ProtocolLib) -> PL
- [Ambassador](https://github.com/adde0109/Ambassador) -> AMB

| Server Type                   | Proxy          | Legacy      | BungeeGuard                | Modern         | Notes |
| ----------------------------- | -------------- | ----------- | -------------------------- | -------------- | --- |
| [Arclight](https://github.com/IzzelAliz/Arclight) 1.14.4-1.0.6         | Velocity (AMB) | No          | No                         | N/A (No PCF)   | Generic forwarding error, malformed data |
| Arclight 1.15.2-1.0.19        | Velocity (AMB) | No          | No                         | N/A (No PCF)   | Bad packet when forwarding, test inconclusive |
| Arclight 1.16.5-1.0.24        | Velocity (AMB) | Yes         | Yes (BG v1.2.2, PL v5.1.0) | Yes (With PCF) | |
|                               | LightFall      |             |                            |                | |
| Arclight 1.17.1-1.0.2         | Velocity (AMB) | No          | No                         | N/A (No PCF)   | Generic forwarding error, malformed data. Would only start when using Java 16 |
|                               | LightFall      |             |                            |                | |
| Arclight 1.18.2-1.0.9         | Velocity (AMB) | No          | No                         | Yes (With PCF) | Generic forwarding error, malformed data |
|                               | LightFall      |             |                            |                | |
| Arclight 1.19.2-1.0.2         | Velocity (AMB) | No          | No                         | Yes (With PCF) | Generic forwarding error, malformed data |
|                               | LightFall      |             |                            |                | |
| Arclight 1.19.3-1.0.3         | Velocity (AMB) | No          | No                         | Yes (With PCF) | Generic forwarding error, malformed data |
|                               | LightFall      |             |                            |                | |
| Arclight 1.19.4-1.0.5         | Velocity (AMB) | No          | No                         | Yes (With PCF 1.19.3) | Generic forwarding error, malformed data |
|                               | LightFall      |             |                            |                | |
| Arclight 1.20.1-1.0.1         | Velocity (AMB) | No          | No                         | Yes (With PCF 1.20) | Generic forwarding error, malformed data |
|                               | LightFall      |             |                            |                | |
| [Magma](https://magmafoundation.org/) 1.12.2-de16e0a9         | Velocity (AMB) |             |                            |                | |
|                               | BungeeCord     |             |                            |                | |
| Magma 1.16.5-36.2.39-c1c5a946 | Velocity (AMB) |             |                            |                | This version is full of bugs and Magma doesn't currently support it |
| Magma 1.18.2-40.2.10-5cda8a26 | Velocity (AMB) |             |                            |                | |
| Magma 1.19.3-44.1.23-6e6ce905 | Velocity (AMB) |             |                            |                | |
| Mohist 1.7.10-46              | Velocity (AMB) | Yes         | N/A                        | N/A            | |
|                               | BungeeCord     |             |                            |                | |
| [Mohist](https://mohistmc.com/) 1.12.2-320             | Velocity (AMB) |             |                            |                | Test failed, server wouldn't connect locally |
|                               | BungeeCord     |             |                            |                | |
| Mohist 1.16.5-1184            | Velocity (AMB) | Yes         | No                         | Yes (With PCF) | Generic forwarding error, malformed data |
| Mohist 1.18.2-86              | Velocity (AMB) |             |                            |                | Test failed, server wouldn't connect locally |
| Mohist 1.19.2-66              | Velocity (AMB) | Yes         | No                         | Yes (With PCF) | Generic forwarding error, malformed data |
| Mohist 1.19.4-196             | Velocity (AMB) |             |                            |                | Test failed, server wouldn't connect locally |
| Mohist 1.20.1-465             | Velocity (AMB) |             |                            |                | Test failed, server wouldn't connect locally |
