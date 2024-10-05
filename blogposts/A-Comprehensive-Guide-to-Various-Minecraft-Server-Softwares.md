# A Comprehensive Guide to Various Minecraft Server Softwares

Please note this guide is comprehensive, but not complete. Some sections were summarized for brevity. If there's a section you'd like added/improved, please let me know!

## Bukkit/Spigot/Paper

Derivatives of Bukkit have generally been the goto server software for many years now, though the original CraftBukkit server software being DMCA'd out of existence in around 2014, Spigot had forked the project (with the same maintainers for the most part), with all the DMCA-able parts removed. Later down the line, Paper forked Spigot and added oodles of performance patches and their own API additons. Folia is a fork of Paper that attempts to multithread the game without corrupting things, and to my knowledge doesn't yet have a public release.

In summary:

- `Bukkit` is the API (Application Program Interface) that developers use for their plugins.
- `CraftBukkit` was the original implementation of the `Bukkit` API
- [`Spigot`](<https://www.spigotmc.org/wiki/spigot-installation/>) is a fork of `CraftBukkit` that adds it's own API features
- [`Paper`](<https://papermc.io/software/paper>) is a fork of `Spigot` that also ads it's own API features
- [`Folia`](<https://papermc.io/software/folia>) is a fork of `Paper` that overhauls the game to attempt at safe-ish multithreading
- The same overall can be said for any other forks of `Spigot`/`Paper`/`Folia`

## Sponge

Sponge is a bit unique, as it originated from a miscellaneous group of people after the 2014 indecent, with the intent of not only replacing Bukkit, but to create a better API for developers to use (This past weekend they just celebrated their 10th anniversary). Sponge's API is completely data driven, which allows for their events to be purely transactional and reversible, which overall is a really neat concept. They prioritize moving forward over maintaining backwards compatibility, which has allowed them to grow and change their API as needed, as opposed to Bukkit/Spigot supporting backwards compatibility as far as to determent the rest of the API (I agree it's cool to never need to change your code, but it limits the overall reach of the API). These ideals allowed Sponge to create SpongeForge; an implementation of the Sponge API that can run in modded (Forge) environments, and a bit later down the line they merged with a project called Granite, which had their own Vanilla-based Sponge API implementation. SpongeVanilla as a server software supports server-side Mixins and runtime Mojang Mappings, which allows developers to easily tweak game-code as needed. To end it off, during their 10th anniversary, they've announced that they're now targeting NeoForge as a Sponge-compatible platform. I must also note that there is a community project Loofah implemting the Sponge API on Fabric, which once complete, will allow Sponge plugins to run on nearly any notable modding platform.
You can find their own post regarding their history [here](<https://docs.spongepowered.org/stable/en/about/history.html>).
Sponge and so many other things would not be possible without [Mumfrey](<https://github.com/Mumfrey>)'s [Mixin](<https://github.com/SpongePowered/Mixin>) library, used in nearly every modern modding project.

In summary:

- the Sponge API is the interface that developers use to create their plugins
- [SpongeForge](<https://spongepowered.org/downloads/spongeforge>) is the Forge implementation of the Sponge API
- [SpongeVanilla](<https://spongepowered.org/downloads/spongevanilla>) is a Vanilla-based implementation of the Sponge API, used in similar places as Bukkit-based servers
- SpongeNeo (no public downloads as of yet) is a NeoForge implemenation of the Sponge API
- [Loofah](<https://github.com/LoofahMC/Loofah>) is a Fabric implementation of the Sponge API

## BungeeCord

Used as a protocol-specific reverse proxy to network multiple Minecraft servers together, BungeeCord wasn't the first, but being created by one of the lead developers of CraftBukkit/Spigot, it quickly gained traction in the community. However, as great as it is and the value that it's added to the community, BungeeCord is not without it's flaws. It's design from the start was insecure and has never been resolved, as the project is currently in maintenance mode. Backend MC servers that utilize legacy forwarding can be connected to using *any* BungeeCord proxy, not just the one you configure yourself. In an insecure network, any assailant can set up their own BungeeCord proxy that "pretends" to be a player with admin privilages (the player names of which you can easily get by pinging the backend server). At that point, I hope you have backups. There are ways to secure your network from these attacks, with the best option being to block the servers at the firewall level, and the second best option being BungeeGuard. Like Bukkit/Spigot, there are many forks of BungeeCord. The most notable being Waterfall by the people over at PaperMC, containing some fixes and better legacy modded client support, which has now been deprecated in favor of Velocity.

In summary:

- [BungeeCord](<https://www.spigotmc.org/wiki/bungeecord/>) is insecure, read their extensive guide [here](<https://www.spigotmc.org/wiki/firewall-guide/>) on securing servers
  - Your firewall is your best defense
  - [BungeeGuard](<https://www.spigotmc.org/resources/bungeeguard.79601/>) is the best alternative
- [Waterfall](<https://github.com/PaperMC/Waterfall>) is a fork with improved legacy (pre 1.13) modded client support and a few other bells and whistles (no longer maintained)
  - [Travertine](<https://github.com/PaperMC/Travertine>) a fork that added 1.7.10 support to WaterFall
  - [lightfall](<https://github.com/ArclightPowered/lightfall>) a fork that implements Forge 1.13+ support specifically for the Arclight Bukkit+Forge hybrid
- [HexaCord](<https://github.com/HexagonMC/BungeeCord>) also no longer maintained, added support for 1.7.10 clients (both vanilla and Forge)

## Velocity

The new-ish proxy kid on the block designed by the people over at PaperMC, Velocity is generally the suggested proxy to use with not only new setups, but existing ones (assuming you can find equivalent plugins). Velocity comes with modern forwarding, which adds a secret to both the proxy and the backend servers that can be used to verify the proxied player's connection. Velocity also supports legacy (BungeeCord) forwarding, along with BungeeGuard forwarding (legacy forwarding with BungeeGuard on the backend servers). Not only is it more secure, Velocity is much faster and properly supports many modern MC features that BungeeCord cannot either due to their legacy codebase. Though something of note is that only Paper/Sponge servers naively support modern forwarding.

In summary:

- [Velocity](<https://papermc.io/software/velocity>) is a modern alternative to BungeeCord
- modern forwarding is much more secure than legacy or BungeeGuard forwarding (BungeeGuard forwarding relies on you remembering to set things up properly which can be missed due to human error).
- Paper/Sponge are the only platforms that naively support modern forwarding

With plugin-based servers and proxies out of the way, it's time to move onto mod-based servers that change the game in more drastic ways.
If you want to learn more about proxies and how they interact with modded servers, check out my post [here](<https://discourse.cubecoders.com/t/minecraft-proxies-and-you/17673>).

## Forge

Forge is an all-around, modder's best friend that goes wayy back to the early days of Minecraft modding. Personally some of the most nostalgic experiences I've had with Minecraft have been with Forge mods. Over the years their modding API has grown, but also accrued quite a bit of tech debt that hasn't been resolved as fast as others would've wanted. As a result, in 2023 there was a split where the bulk of the development team (all of them minus one) split and formed NeoForge. Now, something to note is that Forge did not have an executable Jar from 1.17.1-1.20.2, forcing AMP to generate it's own run script instead of having a select-able Jar. Notable to mod developers, Forge now uses Mojang mappings at runtime for versions 1.20.6+.

In summary:

- [Forge](<https://files.minecraftforge.net/net/minecraftforge/forge/>) has lots of great mods to offer, both new and old
- No select-able server Jar from 1.17.1-1.20.2

## NeoForge

As mentioned, NeoForge split off from Forge in 2023 due to a [variety of reasons](<https://neoforged.net/news/theproject/>), during the MC 1.20.1 release cycle, after which they hard forked in 1.20.2+ with zero intent on backwards compatibility with Forge. The people over at NeoForge suggest using Forge for 1.20.1, as it's gotten more updates than Neo's fork for that version. After 1.20.2 however, there's been a push to use NeoForge, as they've been knocking off quite a bit of dust and making sweeping changes to the developer API (allong with supporting runtime Mojang mappings). NeoForge also does not have a select-able Jar for 1.20.2+.

In summary:

- [NeoForge](<https://neoforged.net/>) split from Forge to invest in their own modding API
- No select-able server Jar

## Fabric

Starting in 1.14, Fabric was born as a lightweight alternative to Forge, a new start learning from Forge's mistakes (their blog post [here](<https://fabricmc.net/2018/12/10/announcement.html>). The primary difference being that there is a clear divide between the FabricLoader and the Fabric API, the former being what loads mods into the game, and the latter being the API that developers can use to create mods more easily and in more compatible ways. You may now notice though, as more and more content mods have moved over to Fabric, you notice less of a performance difference when compared to Forge. This is just the nature of content-heavy mods, the modloader itself is almost always negligible when you're comparing content-mod performance. Quilt is a popular fork of Fabric, though I'm not well versed enough in the controversies to speak on the topic.

In summary:

- [Fabric](<https://fabricmc.net/>) is a wonderful modloader, and offers a variety of interesting mods, many of which being performance inclined
- Fabric's loader and API are two separate programs, as opposed to Forge/Neo's being combined into one for most intents and purposes
- [Quilt](<https://github.com/QuiltMC/quilt-loader>) is a popular fork of Fabric that adds a few of their own APIs while maintaining compatibility with Fabric mods

## Hybrids

Bukkit+Modloader hybrids are a bit of a taboo topic in most places, as they tend to be unstable and cause strange behavior in both mods and plugins alike. If used in moderation, they can be very useful tools, but in most situations it's best to find mods that can replicate the plugin behavior you're looking for to limit the amount of chaos at play.

## Forge + Bukkit

There's a bunch here, so I'll be primarily focusing on what hybrids are best/available for each Minecraft version. I've been working in this space for a bit, so there will be a bit of bias here, fair warning. I may also delve deeper into each at a later date.

Forge Hybrid list:

- [Crucible](<https://github.com/CrucibleMC/Crucible>) - 1.7.10
- [Magma Maintained](<https://github.com/magmamaintained>) - 1.12.2, ~~1.16.5~~, 1.18.2, 1.19.3, ~~1.20.1~~
- [Mohist](<https://mohistmc.com/>) - ~~1.7.10~~, 1.12.2, 1.16.5, 1.18.2, 1.19.2, 1.19.4, 1.20, 1.20.1, 1.20.2
- [Arclight](<https://github.com/IzzelAliz/Arclight>) - 1.14.4, 1.15.2, 1.16.5, 1.17.1, 1.18.2, 1.19.2-1.19.4, 1.20.1-1.20.4, 1.21
- [Ketting](<https://kettingpowered.org/>) - 1.20.1-1.20.4

Suggested:

- 1.7.10 - Crucible
- 1.12.2 - Magma Maintained or Mohist
- 1.14.4 - Arclight
- 1.15.2 - Arclight
- 1.16.5 - Arclight or Mohist
- 1.17.1 - Arclight
- 1.18.2 - Magma Maintained, Arclight, or Mohist
- 1.19.x - Arclight or Mohist
- 1.20.1 - Ketting, Magma Maintained, Arclight, or Mohist
- 1.20.x - Arclight, Ketting, or Mohist
- 1.21 - Don't have a solid suggestion yet

## NeoForge + Bukkit

I'm less versed in this space, but we got the following list of hybrids:

- [Arclight](<https://github.com/IzzelAliz/Arclight>) - 1.20.4-1.21
- [Youer](<https://mohistmc.com/>) - same group as Mohist, TBA
- [Ketting](<https://kettingpowered.org/>) - TBA
- [Magma](<https://magmafoundation.org/>) - TBA

## Fabric + Bukkit

Fabric+Bukkit is the smallest of the bunch, so it's hard to get this wrong:

- [Arclight](<https://github.com/IzzelAliz/Arclight>) - 1.20.4-1.21
- [Banner](<https://mohistmc.com/>) - same group as Mohist, 1.19.4, 1.20, 1.20.1
- [CardBoard](<https://github.com/CardboardPowered/cardboard>) - 1.16.5, 1.18.2, 1.19.2, 1.19.4, 1.20.4, 1.20.6
  - Note, somewhat implements the Paper API, but is inconsistent on updating it when updating the Minecraft version

## TaterLib

Now, at the bottom of the post, I take an opportunity to talk about my own project. [TaterLib](<https://github.com/p0t4t0sandwich/TaterLib>) is a library that developers can use to create mods/plugins that can run across multiple versions of Minecraft, all in a single Jar. Mainly, I define a single common API for every platform/version, and then implement it all by hand. There's a decent amount of repetitive code, but it's quite fun to work on. I've learned some tricks from Sponge on how to implement API interfaces in a somewhat sane manner, and overall it's been a nice project to work on. Currently it supports most modloaders from 1.7.10-1.21.1 (even proxies), along with Forge 1.6.4 and Bukkit b1.7.3. Not a server software in it's own right (yet), but instead sits "on top" of other modloaders in order to do it's thing.
