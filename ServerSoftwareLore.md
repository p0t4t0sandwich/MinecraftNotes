# Server Software Lore

A general summarization how various MC server softwares are related to each other.

If you want a more complete list take a look [here](https://github.com/LeStegii/server-softwares).

## Bukkit

[Bukkit](https://hub.spigotmc.org/stash/projects/SPIGOT/repos/bukkit/browse)

- [CraftBukkit](https://hub.spigotmc.org/stash/projects/SPIGOT/repos/craftbukkit/browse)

  - [Spigot](https://hub.spigotmc.org/stash/projects/SPIGOT/repos/spigot/browse)

    - [Paper](https://github.com/PaperMC/Paper)
   
      - [EmpireCraft](https://github.com/starlis/empirecraft)

      - [Akarin](https://github.com/Akarin-project/Akarin)

      - [Folia](https://github.com/PaperMC/Folia)
     
        - [Kaiiju](https://github.com/KaiijuMC/Kaiiju) -- Folia fork, designed for vanilla/anarchy servers

      - [Purpur](https://github.com/PurpurMC/Purpur)

        -  [MultiPaper](https://github.com/MultiPaper/MultiPaper)

        -  [Patina](https://github.com/PatinaMC/Patina)

      - [Tuinity](https://github.com/Tuinity/Tuinity)
     
        - [Origami](https://github.com/Minebench/Origami)

        - [Yatopia](https://github.com/YatopiaMC/Yatopia)

          - [Airplane](https://github.com/TECHNOVE/Airplane)

            - [Pufferfish](https://github.com/pufferfish-gg/Pufferfish)

              - [Pearl](https://github.com/Pearl-Project/Pearl) -- some optimization and gameplay features that are cherry picked from other projects

              - [Matter](https://github.com/plasmoapp/matter) -- adds a secure feature seed. Based on [Secure Seed](https://github.com/Earthcomputer/SecureSeed) mod by Earthcomputer

              - [Mirai](https://github.com/etil2jz/Mirai) -- a fork of Pufferfish that implements vanilla-friendly Lithium patches

- [Glowstone](https://github.com/GlowstoneMC/Glowstone) -- not a direct fork, as it re-implements the vanilla codebase from scratch, compatible with Bukkit, Spigot, and Paper plugins

## BungeeCord

[BungeeCord](https://github.com/SpigotMC/BungeeCord)

- [HexaCord](https://github.com/HexagonMC/BungeeCord)

- ~~[FlameCord](https://github.com/2lstudios-mc/FlameCord)~~ -- the dev got annoyed at people building from source instead of paying for the server Jar (even though it had an open source licence), and eventually privated the repo

- [Waterfall](https://github.com/PaperMC/Waterfall)

  - [LightFall](https://github.com/ArclightPowered/lightfall) -- Arclight's fork of Waterfall to implement Forge 1.13+ support

  - [Travertine](https://github.com/PaperMC/Travertine) -- Aimed to support 1.7 clients

## Fabric

[Fabric](https://github.com/FabricMC/fabric)

- [Quilt](https://github.com/QuiltMC/quilt-loader)

## Fabric + Bukkit

[Fukkit](https://github.com/FukkitMC/fukkit)

[Cardboard](https://github.com/CardboardPowered/cardboard)

[Banner](https://github.com/MohistMC/Banner)

## Forge

[Forge](https://github.com/MinecraftForge/MinecraftForge)

- [GoldenForge](https://github.com/GoldenForge/GoldenForge) -- aim to implement Paper patches in a stable manner, without plugin support

- [NeoForge](https://github.com/neoforged/NeoForge) -- a hard fork of Forge created by the core team minus one member

## Forge + Bukkit

MCPC+

- [Cauldron](https://sourceforge.net/projects/cauldron-unofficial/files/1.7.10/)

  - [KCauldron](https://github.com/djoveryde/KCauldron)

    - [Uranium](https://github.com/UraniumMC/Uranium)

    - [Thermos](https://github.com/CyberdyneCC/Thermos)

      - [Crucible](https://github.com/CrucibleMC/Crucible)

      - [Mohist](https://github.com/MohistMC/Mohist)

      - [Contigo](https://github.com/djoveryde/Contigo)

        - [Kettle](https://github.com/KettleFoundation/Kettle) -- started as a fork, but changed too much to be considered one

          - [Magma](https://github.com/Hexeption/MagmaArchive) -- created by a former Kettle contributor

            - [Ketting](https://github.com/kettingpowered/Ketting-1-20-x) -- created by a former Magma contributor

            - [Magma Maintained](https://github.com/magmamaintained) -- a maintained fork of Magma that aims to keep everything functional and up to date

[Arclight](https://github.com/IzzelAliz/Arclight)

[BukkitForge](https://github.com/keepcalm/BukkitForge)

~~[FoxServer](https://github.com/Luohuayu/FoxServer)~~ -- stole patches from pretty much everyone, everybody dislikes them, read [here](https://github.com/Luohuayu/FoxServer/issues/7) for some tea
  - ~~[CatServer](https://github.com/Luohuayu/CatServer)~~
  - ~~[LoliServer](https://github.com/LoliServer-MC/LoliServer1.16)~~ -- this gross thing

## HMod

[HMod](https://hey0.net/minecraft/)

- [Canary Classic](https://www.minecraftforum.net/forums/mapping-and-modding-java-edition/minecraft-tools/1261218-mod-canarymod-canary-b11-1-hmod-legacy-1-5-1)

  - [CanaryMod](https://canarymod.net/)

## Lilypad

[Lilypad](https://github.com/LilyPad/GoLilyPad)

## Sponge

[SpongeAPI](https://github.com/SpongePowered/SpongeAPI)
  - [SpongeVanilla](https://github.com/SpongePowered/Sponge/tree/api-10/vanilla)
  - [SpongeForge](https://github.com/SpongePowered/Sponge/tree/api-10/forge)
  - [Lantern](https://github.com/LanternPowered/Lantern)

## Velocity

[Velocity](https://github.com/PaperMC/Velocity)
