# Minecraft Proxies and You

Proxies are the perfect solution if you're looking to lighten the load off a single server, or if you're looking to branch out and support multiple play-styles under one umbrella. Overall this post aims to give a medium-level rundown, keeping the nitty-gritty details for the proxies' official docs. If you want to read more on different server softwares, check out my post [here](<https://discourse.cubecoders.com/t/a-comprehensive-guide-to-various-minecraft-server-softwares/17672>). Overall, a proxy takes in a Minecraft client connection on one port, then directs that player's connection to a multitude of backend servers.

Note, to use a proxy in AMP, your backend servers must have `Standalone Server` disabled in the Minecraft instance's settings.

## Velocity

Yes, I'm putting Velocity first because I'm biased, but also because it has the most info to cover. Velocity offers three forwarding methods: modern, bungeeguard, and legacy (BungeeCord). Modern forwarding is by far the most secure, cryptographically signing the initial player-hello packet that's sent to the backend server when the player switches to said server. BungeeGuard does something similar, but is compatible with legacy forwarding, and is optional on the backend servers. Legacy forwarding is inherently insecure and shouldn't be used if you don't have access to a firewall.

Note, if you want to proxy Forge 1.13+ servers, you must use the [Ambassador](<https://github.com/adde0109/Ambassador>) Velocity plugin.

Good reads:

- [Velocity Docs](<https://docs.papermc.io/velocity/>)
- [Ambassador Readme](<https://github.com/adde0109/Ambassador?tab=readme-ov-file#ambassador>)

## BungeeCord

As mentioned, BungeeCord's default forwarding is insecure without either firewall rules or BungeeGuard, and caution should be taken when setting up BungeeCord (or even just legacy forwarding in general), as someone who's been at the receiving end of UUID-spoofing, it's not fun, and it involves restoring a bunch of backups.

You can forward Arclight 1.14+ servers using the [LightFall-Client](<https://github.com/ArclightPowered/lightfall-client>) mod along with the [LightFall](<https://github.com/ArclightPowered/lightfall>) Waterfall/BungeeCord fork, otherwise modern Forge support is near nonexistant on BungeeCord.

Good reads:

- [BungeeCord Configuration Guide](<https://www.spigotmc.org/wiki/bungeecord-configuration-guide/>)
- [Firewall Guide](<https://www.spigotmc.org/wiki/firewall-guide/>)

## Modern Forwarding

- Overall only supported with 1.13+ servers
- Natively supported by Paper/Sponge
- Supported on Forge 1.14.4-1.21.1 using [Proxy Compatible Forge](<https://modrinth.com/mod/proxy-compatible-forge>) (yes, I do help maintain this one)
- Supported on NeoForge using [Proxy Compatible Forge](<https://modrinth.com/mod/proxy-compatible-forge>) (1.20.2-1.21.1) or [NeoForwarding](<https://modrinth.com/mod/neoforwarding>) (1.20.4-1.21.1)
- Supported on Fabric 1.16.5-1.21.1 using [FabricProxy Lite](<https://modrinth.com/mod/fabricproxy-lite>)
- Supported on some Modloader-Bukkit hybrids, see my other post for a full list. Though it's usually best to let a mod handle it.

## BungeeGuard Forwarding

- Supported on 1.7.10-present
- Supported on Sponge and any Spigot derivative assuming the [BungeeGuard](<https://www.spigotmc.org/resources/bungeeguard.79601/>) plugin supports the version
  - Modloader-Bukkit hybrids implement Spigot and should be compatible as long as [ProtocolLib](<https://www.spigotmc.org/resources/protocollib.1997/>) (a BungeeGuard dependency) can load.

## Legacy Forwarding

- Supported on 1.7.10-present
- Is not secure without firewall rules
- Supported on Sponge and any Spigot derivative
- Supported on most popular Forge versions from 1.7.10-1.20.1 using [BungeeForge](<https://github.com/caunt/BungeeForge>)
- Supported on Fabric 1.16.4-1.18.1 using [FabricProxy](<https://modrinth.com/mod/fabricproxy>), but is no longer maintained in the primary repo
  - [FabricProxy-Legacy](<https://github.com/voruti/FabricProxy-Legacy>)
  - [Fabric-Bungeecord-Proxy](<https://github.com/disymayufei/Fabric-Bungeecord-Proxy>)
  - [ImyvmCircle/FabricProxy](<https://github.com/ImyvmCircle/FabricProxy>)
