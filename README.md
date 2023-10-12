# MinecraftNotes
A repo containing various notes on Minecraft server compatibility, among other things

PRs and issues welcome! Feel free to let me know if you've found a workaround, or if the issue has been patched.

## Proxy Compatibility
### Links
- [Arclight](https://github.com/IzzelAliz/Arclight)
- [Magma](https://magmafoundation.org/)
- [Mohist](https://mohistmc.com/)
- [Velocity](https://papermc.io/downloads/velocity)
- [BungeeCord](https://github.com/SpigotMC/BungeeCord)
- [LightFall](https://github.com/ArclightPowered/lightfall)
- [GoldenForge](https://github.com/GoldenForge/GoldenForge)

### Keys
- Not Applicable -> N/A
- Wouldn't work/needs incompatibility verified -> ---
- Untested -> ?
- [BungeeForge](https://github.com/caunt/BungeeForge) -> BF
- [Proxy Compatible Forge](https://github.com/adde0109/Proxy-Compatible-Forge) -> PCF
- [BungeeGuard](https://github.com/lucko/BungeeGuard) -> BG
- [ProtocolLib](https://github.com/dmulloy2/ProtocolLib) -> PL
- [Ambassador](https://github.com/adde0109/Ambassador) -> AMB
- [LightFallClient](https://github.com/ArclightPowered/lightfall-client/releases) -> LFC
- [UniMixins](https://www.curseforge.com/minecraft/mc-mods/unimixins) -> UNI
### Forge
| Server Type                    | Proxy          | Legacy        | BungeeGuard | Modern         | Notes                                                 |
|--------------------------------|----------------|---------------|-------------|----------------|-------------------------------------------------------|
| Forge 1.7.10-10.13.4.1614      | Velocity       | yes (with UNI)| ---         | N/A            | Need UniMixins to fix mixin issue                     |
|                                | BungeeCord     | ---           | ---         | N/A            |                                                       |
| Forge 1.12.2-14.23.5.2860      | Velocity       | ---           | ---         | N/A            | BungeeForge 1.12.2 doesn't seem to work at the moment |
|                                | BungeeCord     | ---           | ---         | N/A            | BungeeForge 1.12.2 doesn't seem to work at the moment |
| Forge 1.16.5-36.2.39           | Velocity (AMB) | ?             | ?           |                |                                                       |
| Forge 1.18.2-40.2.10           | Velocity (AMB) | Yes (With BF) | N/A         | Yes (With PCF) |                                                       |
| Forge 1.19.2-43.3.2            | Velocity (AMB) | Yes (With BF) | N/A         | Yes (With PCF) |                                                       |
| Forge 1.19.3-44.1.23           | Velocity (AMB) | ?             | ?           | ?              |                                                       |
| Forge 1.19.4-45.2.2            | Velocity (AMB) | ?             | ?           | ?              |                                                       |
| Forge 1.20.1-47.2.1            | Velocity (AMB) | ?             | ?           | ?              |                                                       |
| Forge 1.20.2-48.0.20           | Velocity (AMB) | ?             | ?           | ?              |                                                       |
| GoldenForge 1.19.2-Alpha.0.0.7 | Velocity (AMB) | Yes (With BF) | N/A         | Yes            |                                                       |
| NeoForge 1.20.1-47.1.79        | Velocity (AMB) | ?             | N/A         | ?              |                                                       |

### Forge Hybrids
| Server Type                   | Proxy                                               | Legacy                 | BungeeGuard                | Modern                | Notes                                                                                                                                                                                                                                                                                                                             |
|-------------------------------|-----------------------------------------------------|------------------------|----------------------------|-----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Arclight 1.14.4-1.0.6         | Velocity (AMB)                                      | No                     | No                         | N/A (No PCF)          | Generic forwarding error, malformed data                                                                                                                                                                                                                                                                                          |
| Arclight 1.15.2-1.0.19        | Velocity (AMB)                                      | Yes                    | Yes (BG v1.2.2, PL v5.1.0) | N/A (No PCF)          |                                                                                                                                                                                                                                                                                                                                   |
| Arclight 1.16.5-1.0.24        | Velocity (AMB)                                      | Yes                    | Yes (BG v1.2.2, PL v5.1.0) | Yes (With PCF)        |                                                                                                                                                                                                                                                                                                                                   |
|                               | LightFall                                           | Yes (With LFC 1d4473d) | Yes (BG v1.2.2, PL v5.1.0) | N/A                   |                                                                                                                                                                                                                                                                                                                                   |
| Arclight 1.17.1-1.0.2         | Velocity (AMB)                                      | Yes                    | Yes (BG v1.2.2, PL v5.1.0) | N/A (No PCF)          | Arclight Would only start when using Java 16                                                                                                                                                                                                                                                                                      |
|                               | LightFall                                           | N/A (No LFC)           | N/A (No LFC)               | N/A                   |                                                                                                                                                                                                                                                                                                                                   |
| Arclight 1.18.2-1.0.9         | Velocity (AMB)                                      | Yes                    | No                         | Yes (With PCF)        | Generic forwarding error, malformed data                                                                                                                                                                                                                                                                                          |
|                               | LightFall                                           | Yes (With LFC v1.18-4) | No                         | N/A                   | Generic forwarding error, malformed data                                                                                                                                                                                                                                                                                          |
| Arclight 1.19.2-1.0.2         | Velocity (AMB)                                      | Yes                    | Yes (BG v1.2.2, PL v5.1.0) | Yes (With PCF)        |                                                                                                                                                                                                                                                                                                                                   |
|                               | LightFall                                           | Yes (With LFC v1.19-1) | Yes (BG v1.2.2, PL v5.1.0) | N/A                   |                                                                                                                                                                                                                                                                                                                                   |
| Arclight 1.19.3-1.0.3         | Velocity (AMB)                                      | Yes                    | Yes (BG v1.2.2, PL v5.1.0) | Yes (With PCF)        |                                                                                                                                                                                                                                                                                                                                   |
|                               | LightFall                                           | Yes (With LFC v1.19-2) | Yes (BG v1.2.2, PL v5.1.0) | N/A                   |                                                                                                                                                                                                                                                                                                                                   |
| Arclight 1.19.4-1.0.5         | Velocity (AMB)                                      | Yes                    | Yes (BG v1.2.2, PL v5.1.0) | Yes (With PCF 1.19.3) |                                                                                                                                                                                                                                                                                                                                   |
|                               | LightFall                                           | Yes (With LFC v1.19-3) | Yes (BG v1.2.2, PL v5.1.0) | N/A                   |                                                                                                                                                                                                                                                                                                                                   |
| Arclight 1.20.1-1.0.1         | Velocity (AMB)                                      | Yes                    | Yes (BG v1.2.2, PL v5.1.0) | Yes (With PCF 1.20)   |                                                                                                                                                                                                                                                                                                                                   |
|                               | LightFall                                           | Yes (With LFC v1.20-1) | Yes (BG v1.2.2, PL v5.1.0) | N/A                   |                                                                                                                                                                                                                                                                                                                                   |
| Magma 1.12.2-de16e0a9         | Velocity                                            | ---                    | ---                        | N/A                   | Wouldn't connect, test inconclusive                                                                                                                                                                                                                                                                                               |
|                               | BungeeCord                                          | ---                    | ---                        | N/A                   | Wouldn't connect, test inconclusive                                                                                                                                                                                                                                                                                               |
| Magma 1.16.5-36.2.39-c1c5a946 | Velocity (AMB)                                      | Yes                    | No                         | Yes (With PCF)        | This version is full of bugs and Magma doesn't currently support it                                                                                                                                                                                                                                                               |
| Magma 1.18.2-40.2.10-5cda8a26 | Velocity (AMB)                                      | No                     | No                         | Yes (With PCF)        | AMB + Legacy has some weird problem with `ArgumentPropertyRegistry.deserialize`                                                                                                                                                                                                                                                   |
| Magma 1.19.3-44.1.23-6e6ce905 | Velocity (AMB)                                      | No                     | No                         | Yes                   | Generic forwarding error, malformed data                                                                                                                                                                                                                                                                                          |
| Mohist 1.7.10-46              | Velocity                                            | Yes                    | N/A                        | N/A                   |                                                                                                                                                                                                                                                                                                                                   |
|                               | [Travertine](https://github.com/PaperMC/Travertine) | No                     | N/A                        | N/A                   | Times out, but might work in theory, I can't be bothered to find the most recent working build. For those who want to test, the download url is [this link](https://papermc.io/api/v2/projects/travertine/versions/1.16/builds/BUILD_NUMBER/downloads/travertine-1.16-BUILD_NUMBER.jar) (copy it and substitute the build number) |
|                               | [HexaCord](https://github.com/HexagonMC/BungeeCord) | No                     | N/A                        | N/A                   | Times out, but might work in theory                                                                                                                                                                                                                                                                                               |
| Mohist 1.12.2-320             | Velocity                                            | Yes                    | No                         | N/A                   | Generic forwarding error, malformed data                                                                                                                                                                                                                                                                                          |
|                               | BungeeCord                                          | ---                    | ---                        | N/A                   | Times out, needs verification                                                                                                                                                                                                                                                                                                     |
| Mohist 1.16.5-1184            | Velocity (AMB)                                      | Yes                    | No                         | Yes (With PCF)        | Generic forwarding error, malformed data                                                                                                                                                                                                                                                                                          |
| Mohist 1.18.2-86              | Velocity (AMB)                                      | Yes                    | No                         | Yes (With PCF)        | Generic forwarding error, malformed data                                                                                                                                                                                                                                                                                          |
| Mohist 1.19.2-66              | Velocity (AMB)                                      | Yes                    | No                         | Yes (With PCF)        | Generic forwarding error, malformed data                                                                                                                                                                                                                                                                                          |
| Mohist 1.19.4-196             | Velocity (AMB)                                      | Yes                    | No                         | Yes (With PCF 1.19.3) | Generic forwarding error, malformed data                                                                                                                                                                                                                                                                                          |
| Mohist 1.20.1-465             | Velocity (AMB)                                      | Yes                    | No                         | Yes (With PCF 1.20)   | Generic forwarding error, malformed data                                                                                                                                                                                                                                                                                          |

### Sponge
| Server Type                             | Proxy          | Legacy | BungeeGuard | Modern | Notes |
|-----------------------------------------|----------------|--------|-------------|--------|-------|
| SpongeForge 1.8.9-1890-4.2.0-BETA-1762  | Velocity       | ?      | ?           | N/A    |       |
|                                         | BungeeCord     | ?      | ?           | N/A    |       |
| SpongeForge 1.9.4-1968-5.0.0-BETA-1504  | Velocity       | ?      | ?           | N/A    |       |
|                                         | BungeeCord     | ?      | ?           | N/A    |       |
| SpongeForge 1.10.2-2477-5.2.0-BETA-2793 | Velocity       | ?      | ?           | N/A    |       |
|                                         | BungeeCord     | ?      | ?           | N/A    |       |
| SpongeForge 1.11.2-2476-6.1.0-BETA-2792 | Velocity       | ?      | ?           | N/A    |       |
|                                         | BungeeCord     | ?      | ?           | N/A    |       |
| SpongeForge 1.12.2-2838-7.4.7           | Velocity       | ?      | ?           | N/A    |       |
|                                         | BungeeCord     | ?      | ?           | N/A    |       |
| SpongeForge 1.16.5-36.2.5-8.2.0         | Velocity (AMB) | ?      | ?           | ?      |       |
| SpongeVanilla 1.8.9-4.2.0-BETA-352      | Velocity       | ?      | ?           | N/A    |       |
|                                         | BungeeCord     | ?      | ?           | N/A    |       |
| SpongeVanilla 1.9.4-5.0.0-BETA-83       | Velocity       | ?      | ?           | N/A    |       |
|                                         | BungeeCord     | ?      | ?           | N/A    |       |
| SpongeVanilla 1.10.2-5.2.0-BETA-403     | Velocity       | ?      | ?           | N/A    |       |
|                                         | BungeeCord     | ?      | ?           | N/A    |       |
| SpongeVanilla 1.11.2-6.1.0-BETA-27      | Velocity       | ?      | ?           | N/A    |       |
|                                         | BungeeCord     | ?      | ?           | N/A    |       |
| SpongeVanilla 1.12.2-7.4.7              | Velocity       | ?      | ?           | N/A    |       |
|                                         | BungeeCord     | ?      | ?           | N/A    |       |
| SpongeVanilla 1.15.2-8.0.0-SNAPSHOT     | Velocity       | ?      | ?           | ?      |       |
|                                         | BungeeCord     | ?      | ?           | N/A    |       |
| SpongeVanilla 1.16.5-8.2.0              | Velocity       | ?      | ?           | ?      |       |
|                                         | BungeeCord     | ?      | ?           | N/A    |       |
| SpongeVanilla 1.17.1-9.0.0-RC977        | Velocity       | ?      | ?           | ?      |       |
|                                         | BungeeCord     | ?      | ?           | N/A    |       |
| SpongeVanilla 1.18.2-9.0.0-RC1306       | Velocity       | ?      | ?           | ?      |       |
|                                         | BungeeCord     | ?      | ?           | N/A    |       |
| SpongeVanilla 1.19.2-10.0.0-RC1239      | Velocity       | ?      | ?           | ?      |       |
|                                         | BungeeCord     | ?      | ?           | N/A    |       |
| SpongeVanilla 1.19.3-10.0.0-RC1277      | Velocity       | ?      | ?           | ?      |       |
|                                         | BungeeCord     | ?      | ?           | N/A    |       |
| SpongeVanilla 1.19.4-10.0.0-RC1392      | Velocity       | ?      | ?           | ?      |       |
|                                         | BungeeCord     | ?      | ?           | N/A    |       |
| SpongeVanilla 1.20.1-11.0.0-RC1365      | Velocity       | ?      | ?           | ?      |       |
|                                         | BungeeCord     | ?      | ?           | N/A    |       |
| SpongeVanilla 1.20.2-11.0.0-RC1386      | Velocity       | ?      | ?           | ?      |       |
|                                         | BungeeCord     | ?      | ?           | N/A    |       |

### To Add
- [Cauldron](https://sourceforge.net/projects/cauldron-unofficial/files/1.7.10/)
- [KCauldron](https://github.com/djoveryde/KCauldron)
- [Thermos](https://github.com/CyberdyneCC/Thermos)
- [Uranium](https://github.com/UraniumMC/Uranium)
- MCPC+ ?
- [Fabric](https://github.com/FabricMC/fabric/)
- [Cardboard](https://github.com/CardboardPowered/cardboard)
- [Banner](https://github.com/MohistMC/Banner)
