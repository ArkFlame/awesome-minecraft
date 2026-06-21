<p align="center">
  <img width="400" src="https://raw.githubusercontent.com/sindresorhus/awesome/main/media/logo.svg" alt="Awesome logo">
</p>

<h1 align="center">Awesome Minecraft</h1>

<p align="center">
  A curated, production-oriented index of Minecraft server software, plugins, mods, developer tooling, infrastructure, marketplaces, documentation, and community resources.
</p>

<p align="center">
  <a href="https://github.com/sindresorhus/awesome"><img src="https://awesome.re/badge.svg" alt="Awesome"></a>
  <a href="#contributing"><img src="https://img.shields.io/badge/contributions-welcome-brightgreen.svg" alt="Contributions welcome"></a>
  <a href="#license"><img src="https://img.shields.io/badge/license-CC0%201.0-lightgrey.svg" alt="License CC0 1.0"></a>
</p>

---

## Scope

This list is for Minecraft Java and Bedrock operators, plugin developers, mod developers, network administrators, pack authors, creators, and technical players.

It favors resources that are useful for real servers and real development work: maintained projects, official documentation, source repositories, stable marketplaces, production diagnostics, compatibility tooling, and security-conscious infrastructure.

Not every linked project is open source. Some commercial projects are included because they are widely used or technically relevant. Commercial links are marked when the distinction matters.

---

## Curation Rules

A resource should be included when it satisfies at least one of these conditions:

- It is official, canonical, or maintained by the project owner.
- It is widely used in production Minecraft networks.
- It provides infrastructure, diagnostics, development, security, compatibility, or content-creation value.
- It is historically important and clearly marked as legacy.
- It has enough documentation or source visibility to evaluate before use.

A resource should not be included when it is primarily a piracy launcher, a random direct download, malware-prone, abandoned without historical value, or impossible to evaluate.

---

## Status Legend

- **Recommended** — strong default choice for most users in that category.
- **Specialized** — useful for a specific architecture, version range, or workflow.
- **Commercial** — paid, closed-source, premium, or marketplace-distributed.
- **Legacy** — historically relevant, but not a modern default.
- **Experimental** — useful, but test carefully before production.
- **Caution** — verify maintenance, compatibility, licensing, or trust before use.

---

## Contents

- [Quick Stack Recommendations](#quick-stack-recommendations)
- [Official Minecraft Resources](#official-minecraft-resources)
- [Marketplaces and Distribution](#marketplaces-and-distribution)
- [Server Software](#server-software)
  - [Modern Paper Ecosystem](#modern-paper-ecosystem)
  - [Region-Threaded Servers](#region-threaded-servers)
  - [Vanilla and Semi-Vanilla](#vanilla-and-semi-vanilla)
  - [Modded Servers](#modded-servers)
  - [Hybrid Mod and Plugin Servers](#hybrid-mod-and-plugin-servers)
  - [Alternative Server Implementations](#alternative-server-implementations)
  - [Bedrock Server Software](#bedrock-server-software)
  - [Legacy Server Software](#legacy-server-software)
- [Proxies and Crossplay](#proxies-and-crossplay)
 - [Server Wrappers & Panels](#server-wrappers--panels)
- [Plugins](#plugins)
  - [Core Administration](#core-administration)
  - [Permissions Economy and Placeholders](#permissions-economy-and-placeholders)
  - [Moderation Logging and Rollback](#moderation-logging-and-rollback)
  - [World Editing Building and Creative](#world-editing-building-and-creative)
  - [World Protection Claims and Regions](#world-protection-claims-and-regions)
  - [Performance Diagnostics and Chunk Management](#performance-diagnostics-and-chunk-management)
  - [Protocol Compatibility and Packets](#protocol-compatibility-and-packets)
  - [Security Authentication and Anti-Bot](#security-authentication-and-anti-bot)
  - [Anti-Cheat](#anti-cheat)
  - [NPCs Scripting and Quests](#npcs-scripting-and-quests)
  - [RPG Custom Items Mobs and Resource Packs](#rpg-custom-items-mobs-and-resource-packs)
  - [Chat Tab Scoreboard and Discord](#chat-tab-scoreboard-and-discord)
  - [Maps and Web Views](#maps-and-web-views)
  - [Shops Auctions and Economy Gameplay](#shops-auctions-and-economy-gameplay)
  - [Minigames and Network Gameplay](#minigames-and-network-gameplay)
  - [Plugin Development Libraries](#plugin-development-libraries)
  - [Folia Compatibility Notes](#folia-compatibility-notes)
- [Mods](#mods)
  - [Mod Loaders](#mod-loaders)
  - [Launcher Apps](#launcher-apps)
  - [Client Performance Mods](#client-performance-mods)
  - [Optimization Modpacks](#optimization-modpacks)
  - [Shaders and Visuals](#shaders-and-visuals)
  - [Libraries for Mods](#libraries-for-mods)
- [Clients](#clients)
- [Development](#development)
  - [IDE Plugins and Project Templates](#ide-plugins-and-project-templates)
  - [Build Tooling](#build-tooling)
  - [Mappings Decompilers and Bytecode Tools](#mappings-decompilers-and-bytecode-tools)
  - [Protocol Data and Reverse Engineering](#protocol-data-and-reverse-engineering)
  - [Bots Automation and Headless Clients](#bots-automation-and-headless-clients)
  - [Testing Profiling and Benchmarking](#testing-profiling-and-benchmarking)
- [Content Creation Tools](#content-creation-tools)
  - [Models Textures and Resource Packs](#models-textures-and-resource-packs)
  - [Data Packs Commands and Generators](#data-packs-commands-and-generators)
  - [World Editing and Inspection](#world-editing-and-inspection)
  - [Modpack Authoring](#modpack-authoring)
- [Infrastructure and Operations](#infrastructure-and-operations)
  - [Docker and Containers](#docker-and-containers)
  - [Panels](#panels)
  - [Backups](#backups)
  - [DDoS Protection and Edge Filtering](#ddos-protection-and-edge-filtering)
  - [JVM Tuning](#jvm-tuning)
- [Documentation and Knowledge Bases](#documentation-and-knowledge-bases)
- [Communities](#communities)
- [Server Lists](#server-lists)
- [Legacy Archive](#legacy-archive)
- [Security Notes](#security-notes)
- [Contributing](#contributing)
- [License](#license)

---

## Quick Stack Recommendations

### Modern public survival server

- **Server:** [Paper](https://papermc.io/software/paper) or [Purpur](https://purpurmc.org/)
- **Proxy:** [Velocity](https://papermc.io/software/velocity), if running multiple backends
- **Permissions:** [LuckPerms](https://luckperms.net/)
- **Core commands:** [EssentialsX](https://essentialsx.net/)
- **Rollback:** [CoreProtect](https://www.coreprotect.net/)
- **Protection:** [WorldGuard](https://enginehub.org/worldguard/) or [GriefPrevention](https://github.com/TechFortress/GriefPrevention)
- **Profiling:** [spark](https://spark.lucko.me/)
- **Pregeneration:** [Chunky](https://github.com/pop4959/Chunky)
- **Compatibility:** [ViaVersion](https://viaversion.com/) plus [ViaBackwards](https://github.com/ViaVersion/ViaBackwards), when needed

### High-player spread-out SMP or SkyBlock

- **Server:** [Folia](https://papermc.io/software/folia), only if your plugin set is compatible
- **Profiler:** [spark](https://spark.lucko.me/)
- **Pregeneration:** [Chunky](https://github.com/pop4959/Chunky)
- **Rule:** Do not assume Bukkit plugins are Folia-safe. Region-threaded scheduling changes plugin correctness.

### Modded Java server

- **Loader:** [NeoForge](https://neoforged.net/), [Forge](https://files.minecraftforge.net/), [Fabric](https://fabricmc.net/), or [Quilt](https://quiltmc.org/)
- **Pack management:** [packwiz](https://github.com/packwiz/packwiz)
- **Backups:** [Advanced Backups](https://modrinth.com/project/Jrmoreqs)
- **Profiling:** [spark](https://spark.lucko.me/)
- **Distribution:** [Modrinth](https://modrinth.com/) or [CurseForge](https://www.curseforge.com/minecraft)

### Java plus Bedrock crossplay

- **Bridge:** [Geyser](https://geysermc.org/)
- **Bedrock auth bridge:** [Floodgate](https://geysermc.org/)
- **Proxy option:** [Velocity](https://papermc.io/software/velocity)
- **Rule:** Test interactions, resource packs, custom entities, movement, and inventory behavior. Protocol translation is useful but not perfect.

### Plugin development baseline

- **API target:** Paper API where possible
- **Text:** [Adventure](https://docs.papermc.io/adventure/) and [MiniMessage](https://docs.papermc.io/adventure/minimessage/)
- **Commands:** [cloud](https://cloud.incendo.org/) or [ACF](https://aikar.github.io/commands/)
- **Packets:** [PacketEvents](https://docs.packetevents.com/) or [ProtocolLib](https://github.com/dmulloy2/ProtocolLib)
- **Build:** Gradle or Maven with explicit Java target and dependency shading rules

---

## Official Minecraft Resources

- [Minecraft](https://www.minecraft.net/) — Official Minecraft site.
- [Minecraft Java Server Download](https://www.minecraft.net/en-us/download/server) — Official vanilla Java server download.
- [Minecraft Bedrock Server Download](https://www.minecraft.net/en-us/download/server/bedrock) — Official Bedrock dedicated server download.
- [Minecraft Feedback](https://feedback.minecraft.net/) — Official feedback portal.
- [Minecraft Help Center](https://help.minecraft.net/) — Official support articles.
- [Mojang Bug Tracker](https://bugs.mojang.com/) — Official issue tracker for Minecraft bugs.
- [Minecraft Creator Learning Portal](https://learn.microsoft.com/en-us/minecraft/creator/) — Official Bedrock creator documentation.
- [Mojang API Docs](https://mojang-api-docs.gapple.pw/) — Community-maintained Mojang API documentation.

---

## Marketplaces and Distribution

- [Modrinth](https://modrinth.com/) — Modern distribution platform for mods, plugins, data packs, shaders, resource packs, modpacks, and servers. **Recommended**
- [Hangar](https://hangar.papermc.io/) — PaperMC plugin marketplace for Paper, Velocity, and Waterfall projects. **Recommended**
- [CurseForge](https://www.curseforge.com/minecraft) — Large mod and modpack distribution platform. **Recommended**
- [SpigotMC Resources](https://www.spigotmc.org/resources/) — Long-running Bukkit/Spigot plugin marketplace and forum.
- [Polymart](https://polymart.org/resources) — Plugin and resource marketplace with public and premium resources.
- [BuiltByBit](https://builtbybit.com/resources/) — Marketplace formerly known as MC-Market, covering plugins, setups, builds, configs, and services.
- [Sponge Ore](https://ore.spongepowered.org/) — Sponge plugin repository.
- [Planet Minecraft](https://www.planetminecraft.com/) — Community site for builds, skins, texture packs, data packs, mods, servers, and blogs.

---

## Server Software

### Modern Paper Ecosystem

- [Paper](https://papermc.io/software/paper) — High-performance Minecraft server based on Spigot with an expanded API. **Recommended**
- [Purpur](https://purpurmc.org/) — Paper fork focused on deep gameplay configurability. **Recommended**
- [Pufferfish](https://pufferfish.host/downloads) — Performance-oriented Paper fork with enterprise/performance features. **Specialized**
- [Leaf](https://www.leafmc.one/) — Paper fork focused on performance, vanilla behavior, and stability balance. **Specialized**
- [Spigot](https://www.spigotmc.org/) — High-performance Bukkit-compatible server software. **Legacy-compatible**
- [CraftBukkit](https://dev.bukkit.org/) — Original Bukkit implementation lineage. **Legacy**

### Region-Threaded Servers

- [Folia](https://papermc.io/software/folia) — Paper fork with regionized multithreading. **Specialized**
- [Folia Documentation](https://docs.papermc.io/folia/) — Required reading before building or running Folia-compatible plugins.

Folia is not a drop-in Paper replacement. It is appropriate when players are naturally spread across independent regions and your plugins are written for region-threaded execution.

### Vanilla and Semi-Vanilla

- [Vanilla Server](https://www.minecraft.net/en-us/download/server) — Official Mojang server. **Recommended for baseline testing**
- [Fabric Server](https://fabricmc.net/use/server/) — Lightweight mod-loader server setup for Fabric.
- [Quilt Server](https://quiltmc.org/en/install/server/) — Server installation path for Quilt.
- [SpongeVanilla](https://spongepowered.org/) — Sponge API on a vanilla-style server.

### Modded Servers

- [Fabric](https://fabricmc.net/) — Lightweight modding toolchain and loader. **Recommended**
- [Forge](https://files.minecraftforge.net/) — Long-running Minecraft modding platform with a large legacy and modern ecosystem.
- [NeoForge](https://neoforged.net/) — Community-oriented fork of MinecraftForge and modern modding API. **Recommended for current Forge-family development**
- [Quilt](https://quiltmc.org/) — Fabric-family loader and toolchain. **Specialized**
- [SpongeForge](https://spongepowered.org/) — Sponge API on Forge.

### Hybrid Mod and Plugin Servers

Hybrid servers can load both mods and plugins, but they are not a magic compatibility layer. Test thoroughly before production because Bukkit plugins, Forge/NeoForge/Fabric mods, world lifecycle hooks, entity behavior, mixins, and patched internals can conflict.

- [Arclight](https://github.com/IzzelAliz/Arclight) — Bukkit/Paper-style plugin support on a Forge/NeoForge server. **Caution**
- [Mohist](https://mohistmc.com/) — Hybrid server software for mods and plugins. **Caution**
- [Magma](https://magmafoundation.org/) — Forge plus Bukkit/Paper-style hybrid server. **Caution**
- [Cardboard](https://github.com/CardboardPowered/cardboard) — Bukkit API implementation for Fabric. **Experimental**
- [Banner](https://github.com/MohistMC/Banner) — Fabric plus Bukkit/Paper-style hybrid server. **Experimental**

### Alternative Server Implementations

- [Minestom](https://minestom.net/) — Lightweight Java server implementation for custom game servers, not vanilla drop-in. **Recommended for custom servers**
- [Glowstone](https://glowstone.net/) — Open-source Minecraft server implementation. **Specialized**
- [Cuberite](https://cuberite.org/) — C++ Minecraft-compatible server. **Specialized**
- [Dragonfly](https://github.com/df-mc/dragonfly) — Minecraft Bedrock Edition server software written in Go.
- [Valence](https://github.com/valence-rs/valence) — Rust framework for building Minecraft servers.
- [Pumpkin](https://github.com/Pumpkin-MC/Pumpkin) — Rust Minecraft server implementation. **Experimental**

### Bedrock Server Software

- [Bedrock Dedicated Server](https://www.minecraft.net/en-us/download/server/bedrock) — Official Bedrock dedicated server.
- [PocketMine-MP](https://pmmp.io/) — PHP server software for Minecraft Bedrock Edition.
- [Cloudburst](https://cloudburstmc.org/) — Bedrock server ecosystem and projects.
- [PowerNukkitX](https://github.com/PowerNukkitX/PowerNukkitX) — Java Bedrock server implementation with custom systems.

### Legacy Server Software

- [Airplane](https://github.com/TECHNOVE/Airplane) — Historical Paper fork whose ideas influenced later performance forks. **Legacy**
- [Akarin](https://github.com/Akarin-project/Akarin) — Historical Paper fork. **Legacy**
- [FlamePaper](https://builtbybit.com/resources/flamepaper-high-performance.44405/) — Paper 1.8.8 fork focused on performance, stability, security patches, knockback, tick behavior, and legacy PvP control. **Commercial / Legacy-compatible**
- [TacoSpigot](https://github.com/TacoSpigot/TacoSpigot) — Historical 1.8 PaperSpigot fork. **Legacy**
- [Tuinity](https://github.com/Tuinity/Tuinity) — Historical performance fork merged into Paper. **Legacy**
- [Yatopia](https://github.com/YatopiaMC/Yatopia) — Historical fork, no longer a modern production default. **Legacy**

---

## Proxies and Crossplay

- [Velocity](https://papermc.io/software/velocity) — Modern high-performance proxy by PaperMC. **Recommended**
- [BungeeCord](https://www.spigotmc.org/wiki/bungeecord/) — Original Java server proxy. **Legacy-compatible**
- [Waterfall](https://papermc.io/software/waterfall) — PaperMC BungeeCord fork. PaperMC now marks Waterfall as legacy/discontinued. **Legacy**
- [Travertine](https://github.com/PaperMC/Travertine) — Waterfall fork with 1.7 support. **Legacy**
- [FlameCord](https://flamecord.com/) — BungeeCord/Waterfall-family fork focused on proxy security, anti-bot filtering, firewall workflows, and performance. **Commercial / Specialized**
- [VeloFlame](https://veloflame.com/) — Velocity-family secure proxy fork with anti-bot, account, VPN, rate-limit, and firewall-oriented connection checks. **Commercial / Specialized**
- [Geyser](https://geysermc.org/) — Bridge/proxy allowing Bedrock clients to join Java servers. **Recommended for crossplay**
- [Floodgate](https://geysermc.org/) — Bedrock authentication bridge for Geyser.
- [ViaProxy](https://github.com/ViaVersion/ViaProxy) — ViaVersion standalone proxy for protocol translation and testing.
- [Hopper](https://github.com/BRA1L0R/hopper-rs) — Lightweight Minecraft reverse proxy written in Rust. **Specialized**

---

## Server Wrappers & Panels

- [CubeLauncher](https://github.com/CTPAX4OK/CubeLauncher) - A modern, lightweight, and beautiful open-source desktop launcher template for your Minecraft servers, built with Next.js and Electron.

---

## Plugins

### Core Administration

- [EssentialsX](https://essentialsx.net/) — Core commands, economy, homes, warps, spawn, chat modules, and administration utilities. **Recommended**
- [CMI](https://www.zrips.net/cmi/) — Large commercial administration suite. **Commercial**
- [EssentialsLite](https://builtbybit.com/resources/essentialslite.34917/) — Essentials-style command, homes, warps, kits, economy, menus, and utility suite for Bukkit, Spigot, Paper, and Folia stacks. **Commercial / Specialized**
- [SMP Menus](https://builtbybit.com/resources/smp-menus.108152/) — Configurable inventory menu system for help menus, rules, staff tools, command hubs, and DeluxeMenus-style YAML workflows. **Commercial / Specialized**
- [ServerUtils](https://github.com/AEtherSurfer/ServerUtils) — Utility commands and administration helpers. **Specialized**
- [Plan](https://github.com/plan-player-analytics/Plan) — Player analytics and server activity insights.
- [spark](https://spark.lucko.me/) — Performance profiler for servers, clients, and proxies.

### Permissions Economy and Placeholders

- [LuckPerms](https://luckperms.net/) — Permissions plugin for Bukkit, Sponge, BungeeCord, Velocity, and more. **Recommended**
- [Vault](https://github.com/MilkBowl/VaultAPI) — Economy, permission, and chat bridge API for Bukkit plugins. **Recommended when plugins require it**
- [PlaceholderAPI](https://github.com/PlaceholderAPI/PlaceholderAPI) — Placeholder expansion system for Bukkit/Paper plugins.
- [MiniPlaceholders](https://github.com/MiniPlaceholders/MiniPlaceholders) — Modern MiniMessage-oriented placeholder system.
- [RedisBungee](https://github.com/Limework/RedisBungee) — Redis-backed player synchronization for BungeeCord/Velocity networks.

### Moderation Logging and Rollback

- [CoreProtect](https://www.coreprotect.net/) — Block, inventory, container, and interaction logging with rollback. **Recommended**
- [LiteBans](https://www.spigotmc.org/resources/litebans.3715/) — Network-capable punishment system. **Commercial**
- [AdvancedBan](https://github.com/DevLeoko/AdvancedBan) — Punishment system for Bukkit, BungeeCord, and Velocity.
- [LibertyBans](https://github.com/A248/LibertyBans) — Modern punishment plugin with SQL support.
- [SMP Punishments](https://builtbybit.com/resources/smp-punishments-voice-mute-bans.103696/) — Punishment suite for bans, mutes, kicks, freezes, player history, moderation GUIs, MySQL/SQLite storage, Discord webhooks, and voice mute workflows. **Commercial / Specialized**
- [Ledger](https://github.com/QuiltServerTools/Ledger) — Logging plugin for Fabric servers.
- [InventoryRollbackPlus](https://github.com/danjono/InventoryRollbackPlus) — Restore player inventories after deaths, grief, or accidents.

### World Editing Building and Creative

- [WorldEdit](https://enginehub.org/worldedit/) — World editing tool for builders and administrators. **Recommended**
- [FastAsyncWorldEdit](https://github.com/IntellectualSites/FastAsyncWorldEdit) — High-performance WorldEdit fork for large edits. **Specialized**
- [WorldGuard](https://enginehub.org/worldguard/) — Region protection and rules engine.
- [BuildersUtilities](https://github.com/Arcaniax-Development/Builders-Utilities) — Building utilities for creative workflows.
- [VoxelSniper](https://github.com/IntellectualSites/fastasyncvoxelsniper) — Brush-based terrain and building tool.
- [PlotSquared](https://github.com/IntellectualSites/PlotSquared) — Plot management for creative, prison, and build servers.
- [GoBrush](https://www.spigotmc.org/resources/gobrush.23118/) — Terrain brush plugin. **Commercial / Legacy-compatible**
- [GoPaint](https://www.spigotmc.org/resources/gopaint.27717/) — Painting tool for builders. **Commercial / Legacy-compatible**

### World Protection Claims and Regions

- [WorldGuard](https://enginehub.org/worldguard/) — Region flags and protection. **Recommended**
- [GriefPrevention](https://github.com/TechFortress/GriefPrevention) — Player claim protection for survival servers.
- [Lands](https://github.com/Angeschossen/Lands) — Lands, nations, wars, and claims system. **Commercial ecosystem**
- [Towny](https://github.com/TownyAdvanced/Towny) — Town and nation management plugin.
- [Residence](https://www.spigotmc.org/resources/residence-1-7-10-up-to-1-21.11480/) — Region residence and rental plugin. **Commercial**
- [AdvancedRegionMarket](https://github.com/alex9849/advanced-region-market) — Sell and rent WorldGuard regions.
- [GriefDefender](https://www.spigotmc.org/resources/griefdefender.68900/) — Claim protection for modern servers. **Commercial**
- [HuskClaims](https://github.com/WiIIiam278/HuskClaims) — Lightweight claim plugin for Paper and cross-server setups.
- [SMP Regions](https://builtbybit.com/resources/smp-regions.104646/) — Region flag plugin for SMP servers, warzones, PvP zones, resettable areas, world flags, and Folia-aware region control. **Commercial / Specialized**
- [SMP Protections](https://builtbybit.com/resources/smp-protections.110952/) — Protection-block claiming plugin backed by an SMP Regions-style region engine for survival and competitive SMP servers. **Commercial / Specialized**

### Performance Diagnostics and Chunk Management

- [spark](https://spark.lucko.me/) — CPU, memory, tick, heap, and thread profiling. **Recommended**
- [Chunky](https://github.com/pop4959/Chunky) — Chunk pre-generation for Bukkit/Paper, Fabric, Forge, NeoForge, and Sponge. **Recommended**
- [View Distance Tweaks](https://github.com/froobynooby/ViewDistanceTweaks) — Dynamically adjusts server view distance based on load.
- [FarmControl](https://github.com/froobynooby/FarmControl) — Controls ticking behavior of mobs and farms to reduce lag.
- [EntityDetection](https://github.com/Doclic/EntityDetection) — Entity distribution and debugging utility.
- [VillagerOptimiser](https://github.com/blablubbabc/VillagerOptimiser) — Villager AI optimization. **Caution: version-specific**
- [Mob Farm Manager](https://www.spigotmc.org/resources/mob-farm-manager-supports-1-7-10-up-to-1-21-hopper-support.15127/) — Entity and farm control. **Commercial**
- [EntityLimiter](https://builtbybit.com/resources/entitylimiter-optimize-performance.67164/) — Entity limiting plugin for controlling entity buildup, chunk pressure, and entity-based lag. **Commercial / Specialized**
- [MobStacker](https://builtbybit.com/resources/mobstacker-optimize-server-performance.23141/) — Mob stacking plugin for farms and spawners with configurable exclusions and Folia support. **Commercial / Specialized**
- [RedstoneLimiter](https://builtbybit.com/resources/redstonelimiter-smart-redstone-limiter.23133/) — Redstone limiter for reducing lag-machine impact from pistons, dispensers, lanterns, and other redstone-heavy contraptions. **Commercial / Specialized**

### Protocol Compatibility and Packets

- [ViaVersion](https://viaversion.com/) — Allows newer clients to connect to older server versions. **Recommended**
- [ViaBackwards](https://github.com/ViaVersion/ViaBackwards) — Allows older clients to connect to newer servers.
- [ViaRewind](https://github.com/ViaVersion/ViaRewind) — Adds older protocol support for legacy clients.
- [ProtocolLib](https://github.com/dmulloy2/ProtocolLib) — Packet interception and manipulation library for Bukkit plugins.
- [PacketEvents](https://docs.packetevents.com/) — Modern packet library for Spigot, Paper, Velocity, BungeeCord, Fabric, and Sponge. **Recommended for packet-heavy plugins**
- [Geyser](https://geysermc.org/) — Bedrock-to-Java protocol translation.
- [Floodgate](https://geysermc.org/) — Bedrock auth bridge for Geyser.
- [SkinsRestorer](https://skinsrestorer.net/) — Skin restoration for offline-mode and proxy networks.

### Security Authentication and Anti-Bot

- [AuthMeReloaded](https://github.com/AuthMe/AuthMeReloaded) — Authentication plugin for offline-mode servers. **Specialized**
- [LibreLogin](https://github.com/kyngs/LibreLogin) — Modern authentication plugin for Bukkit/Paper and proxies.
- [FastLogin](https://github.com/games647/FastLogin) — Premium auto-login support for offline-mode servers. **Caution: configure carefully**
- [FlameCord](https://flamecord.com/) — Proxy-level anti-bot and security fork. **Commercial / Specialized**
- [BotSentry](https://www.spigotmc.org/resources/botsentry-the-ultimate-antibot-plugin.55924/) — Anti-bot plugin. **Commercial**
- [TCPShield Plugin](https://github.com/TCPShield/RealIP) — Real IP forwarding support for TCPShield-protected networks.
- [AuthMe Premium](https://builtbybit.com/resources/authme-premium-geyser-java.44493/) — AuthMe add-on for premium-player auto-login, Bungee/Velocity auth flows, and Geyser/Floodgate Bedrock authentication workflows. **Commercial / Specialized**
- [ExploitFixer](https://www.exploitfixer.org/) — Packet exploit, crash-client, malformed packet, invalid NBT, and dupe protection for Spigot, Paper, Folia, and related forks. **Commercial / Specialized**

### Anti-Cheat

Anti-cheat quality depends on server version, movement model, latency, combat design, checks enabled, config quality, and bypass maintenance. Treat every anti-cheat as an engineering component, not a one-click solution.

- [Grim Anticheat](https://grim.ac/) — Simulation-based open-source anti-cheat for modern and legacy versions. **Recommended**
- [GrimAC on Modrinth](https://modrinth.com/project/LJNGWSvH) — Modrinth distribution page for GrimAC.
- [Updated NoCheatPlus](https://github.com/Updated-NoCheatPlus/NoCheatPlus) — Community-maintained NoCheatPlus fork. **Legacy-compatible**
- [AntiCheatAddition](https://github.com/Photon-GitHub/AntiCheatAddition) — Add-on checks commonly paired with other anti-cheats.
- [Themis](https://modrinth.com/plugin/themis) — Lightweight anti-cheat. **Specialized**
- [Vulcan](https://www.spigotmc.org/resources/vulcan-advanced-cheat-detection-1-7-1-21-5.83626/) — Paid anti-cheat. **Commercial**
- [Matrix](https://matrix.rip/) — Paid anti-cheat. **Commercial**
- [Spartan](https://www.vagdedes.com/) — Paid anti-cheat. **Commercial**
- [FairPlay](https://fairplay.arkflame.com/) — Combat-focused anti-cheat for Spigot, Paper, Bukkit, Folia, and Purpur with PacketEvents tracking, combat checks, and mitigation workflows. **Commercial / Specialized**

### NPCs Scripting and Quests

- [Citizens](https://github.com/CitizensDev/Citizens2) — NPC framework for Bukkit/Paper servers. **Recommended**
- [Denizen](https://github.com/DenizenScript/Denizen) — Scripting engine built around Citizens and server automation.
- [Sentinel](https://github.com/mcmonkeyprojects/Sentinel) — Combat NPC add-on for Citizens.
- [Skript](https://github.com/SkriptLang/Skript) — High-level scripting language for Bukkit servers.
- [BetonQuest](https://github.com/BetonQuest/BetonQuest) — Questing system for RPG servers.
- [Quests](https://github.com/PikaMug/Quests) — Quest system with objectives and rewards.
- [BeautyQuests](https://github.com/SkytAsul/BeautyQuests) — GUI-based quests plugin.

### RPG Custom Items Mobs and Resource Packs

- [MythicMobs](https://mythiccraft.io/) — Custom mobs, bosses, skills, and mechanics. **Commercial ecosystem**
- [Model Engine](https://mythiccraft.io/) — Custom entity models and animations. **Commercial ecosystem**
- [ItemsAdder](https://itemsadder.devs.beer/) — Custom items, blocks, GUIs, HUDs, and resource-pack generation. **Commercial**
- [Oraxen](https://docs.oraxen.com/) — Custom items and blocks with resource-pack generation. **Open source / Commercial distribution**
- [Nexo](https://polymart.org/resource/nexo.6901) — Custom items, blocks, furniture, and resource-pack tooling. **Commercial**
- [MMOItems](https://www.mythiccraft.io/index.php?resources/mmoitems.1/) — Custom item system for RPG servers. **Commercial**
- [MMOCore](https://www.mythiccraft.io/index.php?resources/mmocore.4/) — RPG classes, skills, and progression. **Commercial**
- [ExecutableItems](https://www.spigotmc.org/resources/custom-items-free-executable-items.77578/) — Custom item actions and logic.
- [MythicCrucible](https://mythiccraft.io/) — Item and resource-pack ecosystem around MythicCraft. **Commercial**

### Chat Tab Scoreboard and Discord

- [Adventure](https://docs.papermc.io/adventure/) — Modern text, titles, boss bars, sounds, books, and UI components.
- [MiniMessage](https://docs.papermc.io/adventure/minimessage/) — User-friendly text component format.
- [TAB](https://github.com/NEZNAMY/TAB) — Tablist, nametags, scoreboard, bossbar, and layout management. **Commercial ecosystem**
- [DiscordSRV](https://github.com/DiscordSRV/DiscordSRV) — Discord and Minecraft chat bridge.
- [DiscordFlow](https://builtbybit.com/resources/discordflow-role-sync-chat-voice.79503/) — Discord integration plugin for chat sync, role sync, console access, proxy synchronization, and proximity voice workflows. **Commercial / Specialized**
- [VentureChat](https://www.spigotmc.org/resources/venturechat.771/) — Chat channels and formatting.
- [InteractiveChat](https://www.spigotmc.org/resources/interactivechat.75870/) — Interactive chat items, inventory, and cross-server chat features.
- [HuskChat](https://github.com/WiIIiam278/HuskChat) — Cross-server chat plugin.
- [MiniMOTD](https://github.com/jpenilla/MiniMOTD) — MOTD plugin using MiniMessage for servers and proxies.

### Maps and Web Views

- [BlueMap](https://bluemap.bluecolored.de/) — 3D web map renderer for Minecraft worlds. **Recommended**
- [Dynmap](https://github.com/webbukkit/dynmap) — Browser-based map for Minecraft servers.
- [Pl3xMap](https://github.com/pl3xgaming/Pl3xMap) — Lightweight web map for Paper servers. **Check maintenance**
- [Squaremap](https://github.com/jpenilla/squaremap) — Web map designed as a modern Dynmap alternative.
- [ChunkyMap](https://github.com/leMaik/ChunkyMap) — Photorealistic Dynmap renderer powered by Chunky.

### Shops Auctions and Economy Gameplay

- [Shopkeepers](https://github.com/Shopkeepers/Shopkeepers) — Villager-style shop system.
- [QuickShop-Hikari](https://github.com/Ghost-chu/QuickShop-Hikari) — Chest shop plugin.
- [EconomyShopGUI](https://github.com/Gypopo/EconomyShopGUI) — GUI shop plugin.
- [ExcellentShop](https://github.com/nulli0n/ExcellentShop-spigot) — Modern shop plugin. **Commercial ecosystem**
- [AuctionHouse](https://www.zrips.net/auctionhouse/) — Auction house plugin. **Commercial**
- [PlayerWarps](https://www.spigotmc.org/resources/playerwarps.66692/) — Player warp economy plugin. **Commercial**
- [CrazyCrates](https://github.com/Crazy-Crew/CrazyCrates) — Crates plugin.
- [SMP Harvest](https://builtbybit.com/resources/smp-harvest.26872/) — Farming and harvesting progression plugin with upgradable hoes, XP, token rewards, crop rewards, events, zones, and Folia support. **Commercial / Specialized**
- [HarvestableBlocks](https://builtbybit.com/resources/harvestableblocks-block-farm-regen.70601/) — Regenerating block and crop zone plugin for mines, farms, spawns, RPG hubs, and protected harvesting areas. **Commercial / Specialized**

### Minigames and Network Gameplay

- [BedWars1058](https://github.com/andrei1058/BedWars1058) — BedWars minigame plugin.
- [Screaming BedWars](https://github.com/ScreamingSandals/BedWars) — BedWars implementation.
- [TheBridge](https://www.spigotmc.org/resources/bridges-minigame.71678/) — Bridge minigame. **Commercial**
- [Duels](https://www.spigotmc.org/resources/duels.20171/) — Duels plugin. **Commercial**
- [UhcCore](https://www.spigotmc.org/resources/uhccore-automated-uhc-for-minecraft-1-8-1-21.47572/) — UHC automation plugin. **Commercial**
- [HuskHomes](https://github.com/WiIIiam278/HuskHomes) — Cross-server homes, warps, and teleport requests.
- [SMP Combat](https://builtbybit.com/resources/smp-combat.103978/) — Combat tag, combat logging, PvP restrictions, elytra control, pearl restrictions, punishment handling, and legacy-combat profile plugin. **Commercial / Specialized**
- [SMP Lifesteal](https://builtbybit.com/resources/smp-lifesteal.106855/) — Lifesteal core with hearts, revives, rebirths, life-bans, heart items, migration tools, storage options, and Folia-aware scheduling. **Commercial / Specialized**
- [FlamePractice](https://builtbybit.com/resources/flamepractice-duels-ranked-ffa.70252/) — Practice PvP core for duels, ranked modes, FFA, kits, arenas, and competitive network gameplay. **Commercial / Specialized**
- [FlamePearls](https://builtbybit.com/resources/flamepearls-fix-ender-pearl-glitch.27842/) — Ender pearl control plugin for fixing pearl glitching, limiting stasis behavior, and configuring pearl cooldowns, damage, effects, and messages. **Commercial / Specialized**
- [SquidGameX](https://builtbybit.com/resources/squidgamex-run-massive-events-no-lag.66200/) — Event minigame plugin for multi-arena Squid Game-style sessions, voting, cosmetics, progression, and network routing. **Commercial / Specialized**

### Plugin Development Libraries

- [Adventure](https://github.com/PaperMC/adventure) — Server-side UI library for Minecraft Java Edition. **Recommended**
- [cloud](https://cloud.incendo.org/) — JVM command framework with Minecraft platform integrations. **Recommended**
- [ACF](https://aikar.github.io/commands/) — Annotation Command Framework for Bukkit and other JVM platforms.
- [PacketEvents](https://docs.packetevents.com/) — Packet processing/transmission library for multiple Minecraft platforms. **Recommended**
- [ProtocolLib](https://github.com/dmulloy2/ProtocolLib) — Packet library for Bukkit/Spigot/Paper.
- [Triumph GUI](https://github.com/TriumphTeam/triumph-gui) — Inventory GUI library.
- [InventoryFramework](https://github.com/stefvanschie/IF) — Inventory GUI framework.
- [Configurate](https://github.com/SpongePowered/Configurate) — Configuration library from the Sponge ecosystem.
- [bstats](https://bstats.org/) — Metrics platform for Minecraft plugins and mods.
- [paperweight-userdev](https://docs.papermc.io/paper/dev/userdev/) — Paper development setup for plugins needing internals.

### Folia Compatibility Notes

A plugin is not Folia-safe merely because it starts on Folia. Check whether it uses region schedulers correctly and avoids cross-region world access.

High-risk areas:

- Teleportation across worlds or distant regions.
- Entity tracking and combat checks.
- NPC systems.
- WorldEdit-style mass block changes.
- Global synchronous Bukkit scheduler usage.
- Static caches of world/entity/player state.
- Direct Bukkit API access from async threads.

Useful references:

- [Folia Documentation](https://docs.papermc.io/folia/)
- [Folia Plugin List](https://github.com/BlockhostOfficial/folia-plugins)

---

## Mods

### Mod Loaders

- [Fabric](https://fabricmc.net/) — Lightweight, fast-updating modding toolchain. **Recommended**
- [Forge](https://files.minecraftforge.net/) — Long-running mod loader with a large legacy ecosystem.
- [NeoForge](https://neoforged.net/) — Modern Forge-family mod loader and API. **Recommended for new Forge-family projects**
- [Quilt](https://quiltmc.org/) — Fabric-family mod loader and ecosystem. **Specialized**
- [Sponge](https://spongepowered.org/) — Plugin API for modded and vanilla-style servers.
- [LiteLoader](http://www.liteloader.com/) — Historical lightweight loader. **Legacy**

### Launcher Apps

- [Official Minecraft Launcher](https://www.minecraft.net/en-us/download) — Official launcher. **Recommended baseline**
- [Prism Launcher](https://prismlauncher.org/) — Open-source launcher for managing instances, accounts, and mods. **Recommended**
- [Modrinth App](https://modrinth.com/app) — Open-source launcher integrated with Modrinth.
- [ATLauncher](https://atlauncher.com/) — Long-running launcher with modpack support.
- [GDLauncher](https://gdlauncher.com/) — Modern launcher with modpack workflows.
- [MultiMC](https://multimc.org/) — Lightweight instance-based launcher. **Legacy / power-user**
- [CurseForge App](https://www.curseforge.com/download/app) — CurseForge modpack launcher.
- [FTB App](https://www.feed-the-beast.com/ftb-app) — Feed The Beast launcher.

Avoid launchers that bypass Microsoft/Mojang authentication or request credentials in non-standard ways.

### Client Performance Mods

- [Sodium](https://modrinth.com/project/AANobbMI) — Rendering optimization mod. **Recommended**
- [Lithium](https://modrinth.com/mod/lithium) — Game logic optimization mod.
- [FerriteCore](https://modrinth.com/mod/ferrite-core) — Memory usage optimization.
- [ModernFix](https://modrinth.com/mod/modernfix) — Performance, memory, and bug-fix mod for modern Minecraft.
- [ImmediatelyFast](https://modrinth.com/mod/immediatelyfast) — Immediate-mode rendering optimizations.
- [Entity Culling](https://modrinth.com/mod/entityculling) — Skips rendering hidden entities/block entities.
- [Krypton](https://modrinth.com/mod/krypton) — Network stack optimization.
- [C2ME](https://modrinth.com/mod/c2me-fabric) — Chunk generation/loading multithreading. **Experimental**
- [MemoryLeakFix](https://modrinth.com/mod/memoryleakfix) — Fixes known memory leaks.
- [Starlight](https://modrinth.com/mod/starlight) — Lighting engine rewrite. **Legacy for newer versions where lighting changes are integrated elsewhere**
- [Embeddium](https://modrinth.com/mod/embeddium) — Sodium-family renderer for Forge/NeoForge ecosystems.
- [Oculus](https://modrinth.com/mod/oculus) — Iris-compatible shaders for Forge/NeoForge.

### Optimization Modpacks

- [Fabulously Optimized](https://modrinth.com/project/1KVo5zza) — Performance and graphics optimization modpack with OptiFine-like features. **Recommended**
- [Simply Optimized](https://modrinth.com/project/IWnOJA2V) — Lightweight optimization-first modpack.
- [Adrenaline](https://modrinth.com/modpack/adrenaline) — Performance-focused client modpack.
- [Additive](https://modrinth.com/modpack/additive) — Optimization and quality-of-life pack.

### Shaders and Visuals

- [Iris Shaders](https://irisshaders.dev/) — Modern shader loader compatible with many OptiFine shader packs. **Recommended**
- [Iris on Modrinth](https://modrinth.com/project/YL57xq9U) — Modrinth distribution page.
- [OptiFine](https://optifine.net/home) — Historical optimization and shader mod. **Legacy / compatibility caution**
- [Complementary Shaders](https://www.complementary.dev/) — Popular shader pack family.
- [BSL Shaders](https://www.curseforge.com/minecraft/shaders/bsl-shaders) — Popular shader pack.
- [Sildur's Shaders](https://sildurs-shaders.github.io/) — Shader pack family.

### Libraries for Mods

- [Fabric API](https://modrinth.com/mod/fabric-api) — Core hooks and interoperability APIs for Fabric mods.
- [Architectury API](https://modrinth.com/mod/architectury-api) — Cross-loader abstraction API.
- [Cloth Config API](https://modrinth.com/mod/cloth-config) — Config screen library.
- [Mod Menu](https://modrinth.com/mod/modmenu) — Adds mod list and config entry points for Fabric.
- [owo-lib](https://modrinth.com/mod/owo-lib) — Utility library for Fabric mods.
- [Puzzles Lib](https://modrinth.com/mod/puzzles-lib) — Multi-loader utility library.
- [GeckoLib](https://modrinth.com/mod/geckolib) — Animation library for entities, blocks, items, and armor.
- [Curios API](https://www.curseforge.com/minecraft/mc-mods/curios) — Equipment slot API for Forge/NeoForge.
- [Trinkets](https://modrinth.com/mod/trinkets) — Equipment slot API for Fabric.

---

## Clients

These are client distributions or client-side platforms. Many are closed-source. Treat them as convenience products, not development APIs.

- [Lunar Client](https://www.lunarclient.com/) — PvP and performance-focused client. **Commercial / closed-source**
- [Badlion Client](https://client.badlion.net/) — PvP and cosmetics client. **Commercial / closed-source**
- [LabyMod](https://www.labymod.net/) — Client platform with add-ons, cosmetics, and server integrations.
- [Feather Client](https://feathermc.com/) — Modded client with server hosting integrations. **Commercial / closed-source**
- [Essential](https://essential.gg/) — Social, cosmetics, screenshots, and world-hosting client mod.

Removed from the main list: random direct downloads, abandoned PvP clients, and clients distributed through untrusted file hosts.

---

## Development

### IDE Plugins and Project Templates

- [Minecraft Development for IntelliJ IDEA](https://mcdev.io/) — IntelliJ plugin for Minecraft mod and plugin development. **Recommended**
- [PaperMC Starter](https://docs.papermc.io/paper/dev/project-setup/) — Paper plugin project setup docs.
- [Fabric Example Mod](https://github.com/FabricMC/fabric-example-mod) — Minimal Fabric mod template.
- [NeoForge ModDevGradle Example](https://github.com/neoforged/ModDevGradle) — NeoForge Gradle tooling examples.
- [Architectury Templates](https://github.com/architectury/architectury-templates) — Multi-loader mod templates.

### Build Tooling

- [Gradle](https://gradle.org/) — Common JVM build tool for plugins and mods.
- [Maven](https://maven.apache.org/) — Common JVM build tool for plugins.
- [paperweight-userdev](https://docs.papermc.io/paper/dev/userdev/) — Paper internals development support.
- [Fabric Loom](https://github.com/FabricMC/fabric-loom) — Gradle plugin for Fabric development.
- [ForgeGradle](https://github.com/MinecraftForge/ForgeGradle) — Gradle tooling for Forge.
- [ModDevGradle](https://github.com/neoforged/ModDevGradle) — Gradle tooling for NeoForge.
- [Architectury Loom](https://github.com/architectury/architectury-loom) — Multi-loader mod development.
- [Shadow](https://github.com/GradleUp/shadow) — Gradle plugin for shading dependencies.
- [SpecialSource](https://github.com/md-5/SpecialSource) — Remapping tool used in Bukkit/Spigot ecosystems.

### Mappings Decompilers and Bytecode Tools

- [Yarn](https://github.com/FabricMC/yarn) — Open Minecraft mappings for Fabric development.
- [ParchmentMC](https://parchmentmc.org/) — Community parameter and javadoc mappings.
- [mappings.dev](https://mappings.dev/) — Browser for official Minecraft mappings.
- [Linkie](https://linkie.shedaniel.dev/mappings) — Mapping lookup across mapping namespaces.
- [Vineflower](https://github.com/Vineflower/vineflower) — Java decompiler.
- [CFR](https://www.benf.org/other/cfr/) — Java decompiler.
- [Recaf](https://github.com/Col-E/Recaf) — Java bytecode editor.
- [Bytecode Viewer](https://github.com/Konloch/bytecode-viewer) — Bytecode viewer and decompiler frontend.

### Protocol Data and Reverse Engineering

- [Minecraft Wiki Protocol Documentation](https://minecraft.wiki/w/Java_Edition_protocol) — Current protocol documentation after the wiki.vg merge.
- [Protocol History](https://minecraft.wiki/w/Java_Edition_protocol/History) — Protocol change history.
- [PrismarineJS minecraft-data](https://github.com/PrismarineJS/minecraft-data) — Versioned Minecraft data for clients, servers, and libraries. **Recommended**
- [node-minecraft-protocol](https://github.com/PrismarineJS/node-minecraft-protocol) — JavaScript protocol parser/serializer and client/server library.
- [wiki.vg Archive](https://c4k3.github.io/wiki.vg/) — Historical mirror of wiki.vg documentation. **Legacy**
- [Burger](https://github.com/Pokechu22/Burger) — Extracts data from Minecraft jars.
- [Minestom Data](https://github.com/Minestom/VanillaReimplementation) — Useful reference for custom server implementations.

### Bots Automation and Headless Clients

- [Mineflayer](https://github.com/PrismarineJS/mineflayer) — High-level JavaScript API for creating Minecraft bots. **Recommended**
- [Prismarine Viewer](https://github.com/PrismarineJS/prismarine-viewer) — Web viewer for Mineflayer bots and worlds.
- [Baritone](https://github.com/cabaletta/baritone) — Pathfinding automation project. **Caution: server rules and ethics**
- [MCProtocolLib](https://github.com/GeyserMC/MCProtocolLib) — Java protocol library maintained by the GeyserMC ecosystem.
- [SteveProxy](https://github.com/PrismarineJS/node-minecraft-protocol/tree/master/examples) — Example proxy use cases through PrismarineJS tooling.

### Testing Profiling and Benchmarking

- [spark](https://spark.lucko.me/) — Production profiler for Minecraft. **Recommended**
- [JFR](https://docs.oracle.com/javacomponents/jmc-5-4/jfr-runtime-guide/about.htm) — Java Flight Recorder for JVM profiling.
- [VisualVM](https://visualvm.github.io/) — JVM profiling and monitoring tool.
- [YourKit Java Profiler](https://www.yourkit.com/java/profiler/) — Commercial Java profiler.
- [Async Profiler](https://github.com/async-profiler/async-profiler) — Low-overhead Java profiler.
- [mclogs](https://mclo.gs/) — Minecraft log sharing and analysis.
- [Geyser Dump Viewer](https://dump.geysermc.org/) — Geyser configuration and debug dump viewer.

---

## Content Creation Tools

### Models Textures and Resource Packs

- [Blockbench](https://www.blockbench.net/) — Low-poly model editor used heavily for Minecraft models. **Recommended**
- [Blockbench GitHub](https://github.com/JannisX11/blockbench) — Source repository.
- [PackSquash](https://github.com/ComunidadAylas/PackSquash) — Resource and data pack optimizer. **Recommended**
- [OptiGUI](https://modrinth.com/mod/optigui) — Custom GUI texture rules.
- [Animated Java](https://animated-java.dev/) — Blockbench animation workflow for Java Edition.
- [Mine-imator](https://www.mineimator.com/) — Minecraft animation software.
- [Chunky](https://chunky-dev.github.io/docs/) — Path-traced Minecraft renderer.

### Data Packs Commands and Generators

- [misode Data Pack Generators](https://misode.github.io/) — Data pack, worldgen, loot table, predicate, and command generators. **Recommended**
- [MCStacker](https://mcstacker.net/) — Command generator for Java Edition. **Recommended**
- [Minecraft Tools](https://minecraft.tools/) — Command and JSON text generators.
- [Data Pack Upgrader](https://misode.github.io/upgrader/) — Data pack migration tooling.
- [Spyglass](https://github.com/SpyglassMC/Spyglass) — Language server and tooling for Minecraft data packs.
- [sandstone](https://github.com/TheMrZZ/sandstone) — TypeScript framework for data packs.

### World Editing and Inspection

- [Amulet Editor](https://www.amuletmc.com/) — World editor for Java and Bedrock worlds. **Recommended**
- [MCA Selector](https://github.com/Querz/mcaselector) — Select, inspect, prune, and edit Minecraft region files.
- [NBTExplorer](https://github.com/jaquadro/NBTExplorer) — NBT editor for Minecraft files.
- [NBT Studio](https://github.com/tryashtar/nbt-studio) — Modern NBT editor.
- [WorldPainter](https://www.worldpainter.net/) — World generation and map painting tool.
- [World Machine](https://www.world-machine.com/) — Terrain generation software used by advanced map creators. **Commercial**
- [Terra](https://github.com/PolyhedralDev/Terra) — World generation platform.

### Modpack Authoring

- [packwiz](https://github.com/packwiz/packwiz) — Git-friendly modpack management with Modrinth and CurseForge support. **Recommended**
- [packwiz-installer](https://packwiz.infra.link/tutorials/installing/packwiz-installer/) — Automatic installation and updates for packwiz packs.
- [Prism Launcher](https://prismlauncher.org/) — Useful for isolated modpack testing.
- [Modrinth App](https://modrinth.com/app) — Useful for Modrinth-first pack workflows.
- [CurseForge App](https://www.curseforge.com/download/app) — Useful for CurseForge pack workflows.
- [PackSquash](https://github.com/ComunidadAylas/PackSquash) — Optimizes generated resource and data packs.

---

## Infrastructure and Operations

### Docker and Containers

- [itzg/docker-minecraft-server](https://github.com/itzg/docker-minecraft-server) — Docker image for Java Edition servers with automatic server/modloader/modpack support. **Recommended**
- [docker-minecraft-server Docs](https://docker-minecraft-server.readthedocs.io/) — Documentation for itzg's Java server image.
- [itzg/docker-minecraft-bedrock-server](https://github.com/itzg/docker-minecraft-bedrock-server) — Containerized Bedrock server.
- [itzg/mc-router](https://github.com/itzg/mc-router) — Routes Minecraft connections by hostname.
- [itzg/mc-monitor](https://github.com/itzg/mc-monitor) — Health check and status utility.
- [Docker Compose](https://docs.docker.com/compose/) — Useful for multi-container server stacks.

### Panels

- [Pterodactyl](https://pterodactyl.io/) — Free open-source game server panel using Docker isolation. **Recommended for hosting providers**
- [Pelican Panel](https://pelican.dev/) — Modern panel inspired by Pterodactyl. **Emerging**
- [PufferPanel](https://pufferpanel.com/) — Free open-source game server management panel.
- [Crafty Controller](https://craftycontrol.com/) — Minecraft-focused server management panel.
- [AMP](https://cubecoders.com/AMP) — Commercial game server management panel.
- [MCSManager](https://mcsmanager.com/) — Web panel for game server management.

### Backups

- [DriveBackupV2](https://github.com/MaxMaeder/DriveBackupV2) — Uploads server backups to Google Drive, OneDrive, Dropbox, FTP, and SFTP.
- [Advanced Backups](https://modrinth.com/project/Jrmoreqs) — Backup mod/plugin with Forge, NeoForge, Fabric, and plugin support.
- [restic](https://restic.net/) — Encrypted backup tool for server directories.
- [Kopia](https://kopia.io/) — Fast encrypted backup tool.
- [rclone](https://rclone.org/) — Syncs backups to cloud storage.

### DDoS Protection and Edge Filtering

- [TCPShield](https://tcpshield.com/) — Minecraft-specific DDoS protection and edge filtering. **Commercial**
- [Infinity-Filter](https://www.infinity-filter.com/) — Minecraft DDoS and anti-bot filtering. **Commercial**
- [Cosmic Guard](https://cosmicguard.com/) — Minecraft DDoS protection provider. **Commercial**
- [FlameCord](https://flamecord.com/) — Proxy fork with anti-bot functionality. **Commercial / Specialized**
- [Gatekeeper](https://www.spigotmc.org/resources/gatekeeper-antivpn.68837/) — Anti-VPN plugin. **Commercial**

### JVM Tuning

- [Aikar's Flags](https://aikar.co/2018/07/02/tuning-the-jvm-g1gc-garbage-collector-flags-for-minecraft/) — Common G1GC tuning flags for Minecraft servers. **Recommended starting point**
- [Paper Optimization Guide](https://docs.papermc.io/paper/aikars-flags) — PaperMC docs reference for JVM flags and tuning.
- [Eclipse Temurin](https://adoptium.net/temurin/releases/) — OpenJDK builds commonly used for Minecraft servers.
- [Azul Zulu](https://www.azul.com/downloads/) — OpenJDK builds.
- [GraalVM](https://www.graalvm.org/) — JVM distribution; test compatibility before use.

---

## Documentation and Knowledge Bases

- [PaperMC Docs](https://docs.papermc.io/) — Paper, Velocity, Folia, Adventure, and Waterfall documentation. **Recommended**
- [Paper API Javadocs](https://jd.papermc.io/paper/) — Paper API reference.
- [Spigot Javadocs](https://hub.spigotmc.org/javadocs/spigot/) — Spigot API reference.
- [Bukkit Javadocs](https://hub.spigotmc.org/javadocs/bukkit/) — Bukkit API reference.
- [Fabric Docs](https://docs.fabricmc.net/) — Official Fabric documentation.
- [Fabric Wiki](https://wiki.fabricmc.net/) — Community-maintained Fabric documentation.
- [Forge Docs](https://docs.minecraftforge.net/) — Forge documentation.
- [NeoForge Docs](https://docs.neoforged.net/) — NeoForge documentation.
- [Quilt Docs](https://quiltmc.org/en/docs/) — Quilt documentation.
- [Sponge Docs](https://docs.spongepowered.org/) — Sponge documentation.
- [Adventure Docs](https://docs.papermc.io/adventure/) — Adventure library documentation.
- [MiniMessage Docs](https://docs.papermc.io/adventure/minimessage/) — MiniMessage syntax and API docs.
- [PacketEvents Docs](https://docs.packetevents.com/) — PacketEvents documentation.
- [Geyser Wiki](https://wiki.geysermc.org/) — Geyser and Floodgate setup docs.
- [Minecraft Wiki](https://minecraft.wiki/) — Community wiki now hosted independently from Fandom. **Recommended**
- [Java Edition Protocol](https://minecraft.wiki/w/Java_Edition_protocol) — Protocol documentation.
- [PrismarineJS Docs](https://prismarinejs.github.io/) — Documentation for PrismarineJS projects.
- [wiki.vg Historical Mirror](https://c4k3.github.io/wiki.vg/) — Historical protocol documentation. **Legacy**

---

## Communities

- [r/admincraft](https://www.reddit.com/r/admincraft/) — Server administration discussions.
- [r/feedthebeast](https://www.reddit.com/r/feedthebeast/) — Modded Minecraft and modpack discussions.
- [r/fabricmc](https://www.reddit.com/r/fabricmc/) — Fabric development and support.
- [SpigotMC Forums](https://www.spigotmc.org/forums/) — Spigot and plugin development forums.
- [PaperMC Discord](https://discord.gg/papermc) — Paper ecosystem support and development.
- [Fabric Discord](https://discord.gg/v6v4pMv) — Fabric community.
- [NeoForge Discord](https://neoforged.net/discord) — NeoForge community.
- [GeyserMC Discord](https://discord.gg/geysermc) — Geyser support and development.
- [Modrinth Discord](https://discord.modrinth.com/) — Modrinth community.
- [Minecraft Commands Discord](https://discord.gg/9wNcfsH) — Commands and data pack community.

---

## Server Lists

Server lists are useful for discovery and marketing, but they vary heavily in quality, paid placement, and bot traffic. Track conversion instead of raw votes.

- [NameMC](https://namemc.com/minecraft-servers) — Server list and profile platform.
- [MinecraftServers.org](https://minecraftservers.org/) — Long-running server list.
- [Minecraft Server List](https://minecraft-server-list.com/) — Server list and voting platform.
- [TopG](https://topg.org/minecraft-servers/) — Server list covering multiple games.
- [Planet Minecraft Servers](https://www.planetminecraft.com/servers/) — Community server listings.
- [Servers-Minecraft](https://servers-minecraft.net/) — Server listing platform.

---

## Legacy Archive

These resources are historically important or still useful for old servers, but they are not clean defaults for new modern setups.

- [MCMarket](https://www.mc-market.org/) — Rebranded/migrated marketplace lineage; use [BuiltByBit](https://builtbybit.com/resources/) for the current platform.
- [Minecraft Fandom Wiki](https://minecraft.fandom.com/wiki/Minecraft_Wiki) — Old wiki host. Prefer [minecraft.wiki](https://minecraft.wiki/).
- [LiteLoader](http://www.liteloader.com/) — Legacy mod loader.
- [ModCoderPack](http://www.modcoderpack.com/) — Historical Minecraft decompilation/mapping toolkit.
- [MCPBot](https://mcpbot.bspk.rs/) — Historical mapping bot.
- [NoCheatPlus](https://github.com/Updated-NoCheatPlus/NoCheatPlus) — Legacy anti-cheat lineage; use current forks only.
- [Akarin](https://github.com/Akarin-project/Akarin) — Legacy server fork.
- [Yatopia](https://github.com/YatopiaMC/Yatopia) — Legacy server fork.
- [Airplane](https://github.com/TECHNOVE/Airplane) — Legacy Paper fork.
- [Waterfall](https://papermc.io/software/waterfall) — Legacy/discontinued BungeeCord fork.
- [Travertine](https://github.com/PaperMC/Travertine) — Legacy 1.7-compatible proxy fork.
- [OptiFine](https://optifine.net/home) — Historically dominant client optimization/shader mod; modern Fabric/NeoForge stacks often prefer Sodium/Iris or Embeddium/Oculus.

---

## Security Notes

- Do not use cracked launchers, random direct downloads, or clients distributed through untrusted file hosts.
- Do not run random plugin jars on production without checking source, reputation, update history, dependencies, and permissions.
- Prefer official project sites, GitHub releases, Modrinth, Hangar, CurseForge, SpigotMC, Polymart, and BuiltByBit over mirror sites.
- For offline-mode networks, put authentication, proxy forwarding, firewall rules, and backend bind addresses under strict review.
- For Velocity, use modern forwarding and configure backend servers correctly.
- Never expose backend Paper/Purpur/Folia servers directly when they trust proxy forwarding.
- Keep backups outside the server machine.
- Test updates on a staging server before production.
- Treat anti-cheat, anti-bot, and DDoS protection as layered systems. No single plugin protects a public network alone.

---

## Contributing

Contributions should improve curation quality, not just add more links.

A good pull request should include:

- The resource name.
- The canonical URL.
- A one-line description.
- The category where it belongs.
- Its status: recommended, specialized, commercial, legacy, experimental, or caution.
- Why it is worth including.
- Whether it is open source, commercial, or closed-source when relevant.

### Entry Format

```md
- [Name](https://example.com/) — Clear one-line description. **Status**
```

### Removal Criteria

A resource may be removed or moved to legacy when:

- It is abandoned and no longer useful.
- It links to malware, piracy, or credential theft risk.
- It has no canonical source or trustworthy distribution path.
- It is superseded by a safer, maintained, or more complete project.
- It exists only as a random file-hosted binary.

---

## License

[CC0 1.0 Universal](https://creativecommons.org/publicdomain/zero/1.0/)

