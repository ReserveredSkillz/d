# d---- Minecraft Crash Report ----
// Surprise! Haha. Well, this is awkward.

Time: 2023-02-12 16:42:02 GMT
Description: Ticking block entity

java.lang.ArrayIndexOutOfBoundsException: 0
    at blusunrize.immersiveengineering.common.blocks.TileEntityMultiblockPart.isDummy(TileEntityMultiblockPart.java:284)
    at blusunrize.immersiveengineering.common.blocks.metal.TileEntityExcavator.TickCentral_TrueITickableUpdate(TileEntityExcavator.java:91)
    at com.github.terminatornl.tickcentral.api.TickHub.trueUpdate(TickHub.java:48)
    at com.github.terminatornl.tickcentral.api.TickInterceptor.redirectUpdate(TickInterceptor.java:24)
    at blusunrize.immersiveengineering.common.blocks.metal.TileEntityExcavator.update(TileEntityExcavator.java)
    at com.zeitheron.hammercore.asm.McHooks.tickTile(McHooks.java:38)
    at net.minecraft.world.World.updateEntities(World.java:1838)
    at net.minecraft.client.Minecraft.runTick(Minecraft.java:1847)
    at net.minecraft.client.Minecraft.runGameLoop(Minecraft.java:1098)
    at net.minecraft.client.Minecraft.run(Minecraft.java:3942)
    at net.minecraft.client.main.Main.main(SourceFile:123)
    at sun.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
    at sun.reflect.NativeMethodAccessorImpl.invoke(Unknown Source)
    at sun.reflect.DelegatingMethodAccessorImpl.invoke(Unknown Source)
    at java.lang.reflect.Method.invoke(Unknown Source)
    at net.minecraft.launchwrapper.Launch.launch(Launch.java:135)
    at net.minecraft.launchwrapper.Launch.main(Launch.java:28)


A detailed walkthrough of the error, its code path and all known details is as follows:
---------------------------------------------------------------------------------------

-- Block entity being ticked --
  Name: immersiveengineering:excavator // blusunrize.immersiveengineering.common.blocks.metal.TileEntityExcavator
  Block type: ID #4090 (tile.immersiveengineering.metal_multiblock // blusunrize.immersiveengineering.common.blocks.metal.BlockMetalMultiblocks // immersiveengineering:metal_multiblock)
  Block data value: 11 / 0xB / 0b1011
  Block location: World: (181,65,2263), Chunk: (at 5,4,7 in 11,141; contains blocks 176,0,2256 to 191,255,2271), Region: (0,4; contains chunks 0,128 to 31,159, blocks 0,0,2048 to 511,255,2559)
  Actual block type: ID #4090 (tile.immersiveengineering.metal_multiblock // blusunrize.immersiveengineering.common.blocks.metal.BlockMetalMultiblocks // immersiveengineering:metal_multiblock)
  Actual block data value: 11 / 0xB / 0b1011
  Block Entity NBT: {ForgeData:{SpongeData:{Creator:{UUIDMost:3220139420045623338L,UUIDLeast:-6597657273274553732L},Notifier:{UUIDMost:3220139420045623338L,UUIDLeast:-6597657273274553732L}}},offset:[I;],facing:0,processQueue:[],mirrored:0b,pos:0,x:181,y:65,ForgeCaps:{"abyssalcraft:itemtransfer":{isRunning:0b,configurations:[]}},z:2263,ifluxEnergy:0,id:"immersiveengineering:excavator",formed:0b,computerOn:2b,redstoneControlInverted:0b}

-- Affected level --
  Level name: MpServer
  All players: 1 total; [GCEntityClientPlayerMP['ReservedSkillz'/318937, l='MpServer', x=188.22, y=63.00, z=2263.09]]
  Chunk stats: MultiplayerChunkCache: 59, 59
  Level seed: 0
  Level generator: ID 00 - default, ver 1. Features enabled: false
  Level generator options: 
  Level spawn location: World: (255,79,255), Chunk: (at 15,4,15 in 15,15; contains blocks 240,0,240 to 255,255,255), Region: (0,0; contains chunks 0,0 to 31,31, blocks 0,0,0 to 511,255,511)
  Level time: 792896697 game time, 767928604 day time
  Level dimension: 0
  Level storage version: 0x00000 - Unknown?
  Level weather: Rain time: 0 (now: true), thunder time: 0 (now: false)
  Level game mode: Game mode: survival (ID 0). Hardcore: false. Cheats: false
  Forced entities: 20 total; [EntityEnderman['Enderman'/317796, l='MpServer', x=177.15, y=31.00, z=2224.78], GCEntityClientPlayerMP['ReservedSkillz'/318937, l='MpServer', x=188.22, y=63.00, z=2263.09], EntityBat['Bat'/262894, l='MpServer', x=186.56, y=26.59, z=2248.31], EntityEnderman['Enderman'/317803, l='MpServer', x=151.32, y=49.00, z=2288.11], EntitySheep['Sheep'/113617, l='MpServer', x=166.52, y=63.00, z=2273.05], EntitySheep['Sheep'/317813, l='MpServer', x=210.80, y=64.00, z=2305.71], EntitySheep['Sheep'/86101, l='MpServer', x=174.33, y=63.00, z=2243.31], EntitySheep['Sheep'/113621, l='MpServer', x=183.69, y=64.00, z=2300.19], EntityItem['item.item.quark:root'/318960, l='MpServer', x=140.88, y=23.00, z=2236.13], EntitySheep['Sheep'/86100, l='MpServer', x=175.17, y=63.00, z=2243.61], EntitySheep['Sheep'/113620, l='MpServer', x=176.75, y=63.00, z=2224.67], EntityItem['item.tile.cloth.white'/86103, l='MpServer', x=173.64, y=63.00, z=2242.10], EntitySheep['Sheep'/113623, l='MpServer', x=181.89, y=64.00, z=2305.84], EntitySheep['Sheep'/86102, l='MpServer', x=175.26, y=63.00, z=2249.14], EntityItem['item.tile.mushroom'/318963, l='MpServer', x=144.14, y=9.00, z=2218.47], EntitySheep['Sheep'/113625, l='MpServer', x=184.24, y=64.00, z=2304.74], EntityItem['item.tile.sapling.oak'/318972, l='MpServer', x=177.32, y=62.00, z=2272.46], EntitySheep['Sheep'/86104, l='MpServer', x=183.21, y=63.00, z=2240.64], EntitySheep['Sheep'/113624, l='MpServer', x=176.58, y=64.00, z=2310.20], EntityItem['item.item.quark:root_black_flower'/318968, l='MpServer', x=166.88, y=40.00, z=2289.25]]
  Retry entities: 0 total; []
  Server brand: ungeecord (git:BungeeCord-Bootstrap:1.18-R0.1-SNAPSHOT:c53fb06:unk
  Server type: Non-integrated multiplayer server

-- System Details --
  Minecraft Version: 1.12.2
  Operating System: Windows 11 (amd64) version 10.0
  Java Version: 1.8.0_361, Oracle Corporation
  Java VM Version: Java HotSpot(TM) 64-Bit Server VM (mixed mode), Oracle Corporation
  Memory: 2519358976 bytes (2402 MB) / 7443841024 bytes (7099 MB) up to 11185160192 bytes (10667 MB)
  JVM Flags: 3 total; -XX:HeapDumpPath=MojangTricksIntelDriversForPerformance_javaw.exe_minecraft.exe.heapdump -Xms1024M -Xmx12000M
  IntCache: cache: 0, tcache: 0, allocated: 0, tallocated: 0
  FML: MCP 9.42 Powered by Forge 14.23.5.2860 269 mods loaded, 269 mods active
       States: 'U' = Unloaded 'L' = Loaded 'C' = Constructed 'H' = Pre-initialized 'I' = Initialized 'J' = Post-initialized 'A' = Available 'D' = Disabled 'E' = Errored
       
       | State  | ID                                | Version                             | Source                                                      | Signature                                |
       |:------ |:--------------------------------- |:----------------------------------- |:----------------------------------------------------------- |:---------------------------------------- |
       | LCHIJA | minecraft                         | 1.12.2                              | minecraft.jar                                               | None                                     |
       | LCHIJA | mcp                               | 9.42                                | minecraft.jar                                               | None                                     |
       | LCHIJA | FML                               | 8.0.99.99                           | forge-1.12.2-14.23.5.2860.jar                               | e3c3d50c7c986df74c645c0ac54639741c90a557 |
       | LCHIJA | forge                             | 14.23.5.2860                        | forge-1.12.2-14.23.5.2860.jar                               | e3c3d50c7c986df74c645c0ac54639741c90a557 |
       | LCHIJA | additionalresources               | 0.1.1                               | additionalresources-1.9.4-0.2.0.28+47cd0bd_signed.jar       | None                                     |
       | LCHIJA | creativecoredummy                 | 1.0.0                               | minecraft.jar                                               | None                                     |
       | LCHIJA | itemphysic                        | 1.4.0                               | minecraft.jar                                               | None                                     |
       | LCHIJA | ivtoolkit                         | 1.3.3-1.12                          | minecraft.jar                                               | None                                     |
       | LCHIJA | micdoodlecore                     |                                     | minecraft.jar                                               | None                                     |
       | LCHIJA | mixinbooter                       | 7.0                                 | minecraft.jar                                               | None                                     |
       | LCHIJA | openmodscore                      | 0.12.2                              | minecraft.jar                                               | None                                     |
       | LCHIJA | bnbgamingcore                     | 0.12.0                              | minecraft.jar                                               | None                                     |
       | LCHIJA | foamfixcore                       | 7.7.4                               | minecraft.jar                                               | None                                     |
       | LCHIJA | tickcentral                       | 3.2                                 | TickCentral-3.2.jar                                         | None                                     |
       | LCHIJA | randompatches                     | 1.12.2-1.22.1.10                    | randompatches-1.12.2-1.22.1.10.jar                          | None                                     |
       | LCHIJA | tweakersconstruct                 | 1.12.2-1.6.1                        | tweakersconstruct-1.12.2-1.6.1.jar                          | None                                     |
       | LCHIJA | forgelin                          | 1.8.4                               | Forgelin-1.8.4.jar                                          | None                                     |
       | LCHIJA | alib                              | 1.0.12                              | alib-1.0.12.jar                                             | None                                     |
       | LCHIJA | wanionlib                         | 1.12.2-2.9                          | WanionLib-1.12.2-2.9.jar                                    | None                                     |
       | LCHIJA | biggercraftingtables              | 1.12.2-2.3b                         | BiggerCraftingTables-1.12.2-2.3b.jar                        | None                                     |
       | LCHIJA | crafttweaker                      | 4.1.20                              | CraftTweaker2-1.12-4.1.20.681.jar                           | None                                     |
       | LCHIJA | alchemistry                       | 1.12.2-42                           | alchemistry-1.12.2-42.jar                                   | None                                     |
       | LCHIJA | endertweaker                      | 1.2.3                               | EnderTweaker-1.12.2-1.2.3.jar                               | None                                     |
       | LCHIJA | mtlib                             | 3.0.7                               | MTLib-3.0.7.jar                                             | None                                     |
       | LCHIJA | modtweaker                        | 4.0.19                              | modtweaker-4.0.20.11.jar                                    | None                                     |
       | LCHIJA | jei                               | 4.16.1.302                          | jei_1.12.2-4.16.1.302.jar                                   | None                                     |
       | LCHIJA | abyssalcraft                      | 1.10.4                              | AbyssalCraft-1.12.2-1.10.4.jar                              | 220f10d3a93b3ff5fbaa7434cc629d863d6751b9 |
       | LCHIJA | ctm                               | MC1.12.2-1.0.2.31                   | CTM-MC1.12.2-1.0.2.31.jar                                   | None                                     |
       | LCHIJA | mysticalworld                     | 1.12.2-1.11.0                       | mysticalworld-1.12.2-1.11.0.jar                             | None                                     |
       | LCHIJA | chisel                            | MC1.12.2-1.0.2.45                   | Chisel-MC1.12.2-1.0.2.45.jar                                | None                                     |
       | LCHIJA | baubles                           | 1.5.2                               | Baubles-1.12-1.5.2.jar                                      | None                                     |
       | LCHIJA | endercore                         | 1.12.2-0.5.76                       | EnderCore-1.12.2-0.5.76.jar                                 | None                                     |
       | LCHIJA | thaumcraft                        | 6.1.BETA26                          | Thaumcraft-1.12.2-6.1.BETA26.jar                            | None                                     |
       | LCHIJA | toolprogression                   | 1.12.2-1.6.12                       | toolprogression-1.12.2-1.6.12.jar                           | e631d7254e451d0360d0148cb21407d5511d45e9 |
       | LCHIJA | codechickenlib                    | 3.2.3.358                           | CodeChickenLib-1.12.2-3.2.3.358-universal.jar               | f1850c39b2516232a2108a7bd84d1cb5df93b261 |
       | LCHIJA | redstoneflux                      | 2.1.1                               | RedstoneFlux-1.12-2.1.1.1-universal.jar                     | None                                     |
       | LCHIJA | cofhcore                          | 4.6.6                               | CoFHCore-1.12.2-4.6.6.1-universal.jar                       | None                                     |
       | LCHIJA | brandonscore                      | 2.4.20                              | BrandonsCore-1.12.2-2.4.20.162-universal.jar                | None                                     |
       | LCHIJA | cofhworld                         | 1.4.0                               | CoFHWorld-1.12.2-1.4.0.1-universal.jar                      | None                                     |
       | LCHIJA | thermalfoundation                 | 2.6.7                               | ThermalFoundation-1.12.2-2.6.7.1-universal.jar              | None                                     |
       | LCHIJA | draconicevolution                 | 2.3.28                              | Draconic-Evolution-1.12.2-2.3.28.354-universal.jar          | None                                     |
       | LCHIJA | thermalexpansion                  | 5.5.7                               | ThermalExpansion-1.12.2-5.5.7.1-universal.jar               | None                                     |
       | LCHIJA | enderio                           | 5.3.70                              | EnderIO-1.12.2-5.3.70.jar                                   | None                                     |
       | LCHIJA | enderiointegrationtic             | 5.3.70                              | EnderIO-1.12.2-5.3.70.jar                                   | None                                     |
       | LCHIJA | mantle                            | 1.12-1.3.3.55                       | Mantle-1.12-1.3.3.55.jar                                    | None                                     |
       | LCHIJA | quark                             | r1.6-179                            | Quark-r1.6-179.jar                                          | None                                     |
       | LCHIJA | twilightforest                    | 3.11.1021                           | twilightforest-1.12.2-3.11.1021-universal.jar               | None                                     |
       | LCHIJA | tconstruct                        | 1.12.2-2.13.0.183                   | TConstruct-1.12.2-2.13.0.183.jar                            | None                                     |
       | LCHIJA | acintegration                     | 1.11.3                              | AbyssalCraft Integration-1.12.2-1.11.3.jar                  | 220f10d3a93b3ff5fbaa7434cc629d863d6751b9 |
       | LCHIJA | fastbench                         | 1.7.4                               | FastWorkbench-1.12.2-1.7.4.jar                              | None                                     |
       | LCHIJA | actuallyadditions                 | 1.12.2-r152                         | ActuallyAdditions-1.12.2-r152.jar                           | None                                     |
       | LCHIJA | actuallybaubles                   | 1.1                                 | ActuallyBaubles-1.12-1.1.jar                                | None                                     |
       | LCHIJA | appliedenergistics2               | rv6-stable-7-extended_life-v0.54.19 | appliedenergistics2-rv6-stable-7-extended_life-v0.54.19.jar | None                                     |
       | LCHIJA | aenetvistool                      | 1.0.3                               | AE-Net-Vis-Tool-1.12.2-1.0.3.0-universal.jar                | None                                     |
       | LCHIJA | projecte                          | 1.12.2-PE1.4.1                      | ProjectE-1.12.2-PE1.4.1.jar                                 | None                                     |
       | LCHIJA | p455w0rdslib                      | 2.3.161                             | p455w0rdslib-1.12.2-2.3.161.jar                             | 186bc454cd122c9c2f1aa4f95611254bcc543363 |
       | LCHIJA | ae2wtlib                          | 1.0.34                              | AE2WTLib-1.12.2-1.0.34.jar                                  | 186bc454cd122c9c2f1aa4f95611254bcc543363 |
       | LCHIJA | aether_legacy                     | 1.5.3.2                             | aether-1.12.2-v1.5.3.2.jar                                  | None                                     |
       | LCHIJA | infinitylib                       | 1.12.2-1.12.1                       | infinitylib-1.12.1.jar                                      | None                                     |
       | LCHIJA | agricraft                         | 2.12.0-1.12.2-b2                    | agricraft-2.12.0-1.12.2-b2.jar                              | None                                     |
       | LCHIJA | akashictome                       | 1.2-12                              | AkashicTome-1.2-12.jar                                      | None                                     |
       | LCHIJA | appleskin                         | 1.0.14                              | AppleSkin-mc1.12-1.0.14.jar                                 | None                                     |
       | LCHIJA | astralsorcery                     | 1.10.27                             | astralsorcery-1.12.2-1.10.27.jar                            | a0f0b759d895c15ceb3e3bcb5f3c2db7c582edf0 |
       | LCHIJA | astral-level-nerf                 | 1.0.1                               | astral-level-nerf-1.0.1-all.jar                             | None                                     |
       | LCHIJA | atum                              | 2.0.20                              | Atum-1.12.2-2.0.20.jar                                      | None                                     |
       | LCHIJA | morphtool                         | 1.2-21                              | Morph-o-Tool-1.2-21.jar                                     | None                                     |
       | LCHIJA | autoreglib                        | 1.3-32                              | AutoRegLib-1.3-32.jar                                       | None                                     |
       | LCHIJA | avaritia                          | 3.3.0                               | Avaritia-1.12.2-3.3.0.37-universal.jar                      | None                                     |
       | LCHIJA | avaritiaddons                     | 1.12.2-1.2                          | Avaritiaddons-1.12.2-1.2.jar                                | None                                     |
       | LCHIJA | badmobs                           | 1.1.40                              | BadMobs-1.12.2-1.1.40.jar                                   | d476d1b22b218a10d845928d1665d45fce301b27 |
       | LCHIJA | badwithernocookiereloaded         | 1.12.2-3.4.18                       | badwithernocookiereloaded-1.12.2-3.4.18.jar                 | None                                     |
       | LCHIJA | base                              | 3.14.0                              | base-1.12.2-3.14.0.jar                                      | None                                     |
       | LCHIJA | bno                               | 1.12.2-1.0.4.0                      | BasicNetherOres-1.12.2-1.0.5.0.jar                          | None                                     |
       | LCHIJA | bhc                               | 1.2.3                               | baubley-heart-canisters-1.12.2-1.2.3.jar                    | None                                     |
       | LCHIJA | betteradvancements                | 0.1.0.77                            | BetterAdvancements-1.12.2-0.1.0.77.jar                      | None                                     |
       | LCHIJA | betterbuilderswands               | 0.13.2                              | BetterBuildersWands-1.12.2-0.13.2.271+5997513.jar           | None                                     |
       | LCHIJA | bettercaves                       | 1.12.2                              | bettercaves-1.12.2-2.0.4.jar                                | None                                     |
       | LCHIJA | betternether                      | 0.1.8.6                             | betternether-0.1.8.6.jar                                    | None                                     |
       | LCHIJA | betterp2p                         | 1.12.2-1.2.3-extended_life          | betterp2p-1.12.2-1.2.3-extended_life.jar                    | None                                     |
       | LCHIJA | betterquesting                    | 3.5.329                             | BetterQuesting-3.5.329.jar                                  | None                                     |
       | LCHIJA | botania                           | r1.10-364                           | Botania r1.10-364.4.jar                                     | None                                     |
       | LCHIJA | dj2addons                         | 1.2.1.1.1                           | dj2addons-1.2.1.1.1.jar                                     | None                                     |
       | LCHIJA | patchouli                         | 1.0-23.6                            | Patchouli-1.0-23.6.jar                                      | None                                     |
       | LCHIJA | bewitchment                       | 0.22.63                             | bewitchment-1.12.2-0.0.22.64.jar                            | None                                     |
       | LCHIJA | bibliocraft                       | 2.4.6                               | BiblioCraft[v2.4.6][MC1.12.2].jar                           | None                                     |
       | LCHIJA | biometweaker                      | 3.2.369                             | BiomeTweaker-1.12.2-3.2.369.jar                             | 631f326344f7f5fd7df7eb940760ebd52b7c9c17 |
       | LCHIJA | guideapi                          | 1.12-2.1.8-63                       | Guide-API-1.12-2.1.8-63.jar                                 | None                                     |
       | LCHIJA | bloodmagic                        | 1.12.2-2.4.3-105                    | BloodMagic-1.12.2-2.4.3-105.jar                             | None                                     |
       | LCHIJA | bnbgaminglib                      | 2.17.6                              | BNBGamingLib-1.12.2-2.17.6.jar                              | None                                     |
       | LCHIJA | bookshelf                         | 2.3.590                             | Bookshelf-1.12.2-2.3.590.jar                                | d476d1b22b218a10d845928d1665d45fce301b27 |
       | LCHIJA | bqtweaker                         | 1.3.3                               | BQTweaker-1.3.3.jar                                         | None                                     |
       | LCHIJA | buildinggadgets                   | 2.8.4                               | BuildingGadgets-2.8.4.jar                                   | None                                     |
       | LCHIJA | chameleon                         | 1.12-4.1.3                          | Chameleon-1.12-4.1.3.jar                                    | None                                     |
       | LCHIJA | chiselsandbits                    | 14.33                               | chiselsandbits-14.33.jar                                    | None                                     |
       | LCHIJA | clumps                            | 3.1.2                               | Clumps-3.1.2.jar                                            | None                                     |
       | LCHIJA | cyclopscore                       | 1.6.7                               | CyclopsCore-1.12.2-1.6.7.jar                                | bd0353b3e8a2810d60dd584e256e364bc3bedd44 |
       | LCHIJA | commoncapabilities                | 2.4.8                               | CommonCapabilities-1.12.2-2.4.8.jar                         | bd0353b3e8a2810d60dd584e256e364bc3bedd44 |
       | LCHIJA | contenttweaker                    | 1.12.2-4.10.0                       | ContentTweaker-1.12.2-4.10.0.jar                            | None                                     |
       | LCHIJA | controlling                       | 3.0.10                              | Controlling-3.0.10.jar                                      | None                                     |
       | LCHIJA | craftingtweaks                    | 8.1.9                               | CraftingTweaks_1.12.2-8.1.9.jar                             | None                                     |
       | LCHIJA | ctgui                             | 1.0.0                               | CraftTweaker2-1.12-4.1.20.681.jar                           | None                                     |
       | LCHIJA | crafttweakerjei                   | 2.0.3                               | CraftTweaker2-1.12-4.1.20.681.jar                           | None                                     |
       | LCHIJA | creativecore                      | 1.9.9                               | CreativeCore_v1.9.19_mc1.12.2.jar                           | None                                     |
       | LCHIJA | cucumber                          | 1.1.3                               | Cucumber-1.12.2-1.1.3.jar                                   | None                                     |
       | LCHIJA | custommainmenu                    | 2.0.9.1                             | CustomMainMenu-MC1.12.2-2.0.9.1.jar                         | None                                     |
       | LCHIJA | wasaila                           | 1.0                                 | Wasaila-1.0.jar                                             | None                                     |
       | LCHIJA | waila                             | 1.8.26                              | Hwyla-1.8.26-B41_1.12.2.jar                                 | None                                     |
       | LCHIJA | mousetweaks                       | 2.10.1                              | MouseTweaks-2.10.1-mc1.12.2.jar                             | None                                     |
       | LCHIJA | danknull                          | 1.7.101                             | DankNull-1.12.2-1.7.101.jar                                 | 644f38521a349310a5dae0239577dc7beebefaec |
       | LCHIJA | journeymap                        | 1.12.2-5.7.1                        | journeymap-1.12.2-5.7.1.jar                                 | None                                     |
       | LCHIJA | defaultoptions                    | 9.2.8                               | DefaultOptions_1.12.2-9.2.8.jar                             | None                                     |
       | LCHIJA | divinerpg                         | 1.7.1                               | DivineRPG-1.7.1.jar                                         | None                                     |
       | LCHIJA | draconicadditions                 | 1.15.1                              | Draconic-Additions-1.12.2-1.15.1.39-universal.jar           | None                                     |
       | LCHIJA | dupefixproject                    | 3.1.6                               | DupeFixProject-1.12.2-3.1.6.jar                             | None                                     |
       | LCHIJA | enderiobase                       | 5.3.70                              | EnderIO-1.12.2-5.3.70.jar                                   | None                                     |
       | LCHIJA | enderioconduits                   | 5.3.70                              | EnderIO-1.12.2-5.3.70.jar                                   | None                                     |
       | LCHIJA | enderioconduitsappliedenergistics | 5.3.70                              | EnderIO-1.12.2-5.3.70.jar                                   | None                                     |
       | LCHIJA | enderioconduitsopencomputers      | 5.3.70                              | EnderIO-1.12.2-5.3.70.jar                                   | None                                     |
       | LCHIJA | enderioconduitsrefinedstorage     | 5.3.70                              | EnderIO-1.12.2-5.3.70.jar                                   | None                                     |
       | LCHIJA | enderiointegrationforestry        | 5.3.70                              | EnderIO-1.12.2-5.3.70.jar                                   | None                                     |
       | LCHIJA | enderiointegrationticlate         | 5.3.70                              | EnderIO-1.12.2-5.3.70.jar                                   | None                                     |
       | LCHIJA | enderioinvpanel                   | 5.3.70                              | EnderIO-1.12.2-5.3.70.jar                                   | None                                     |
       | LCHIJA | ftblib                            | 5.4.7.2                             | FTBLib-5.4.7.2.jar                                          | None                                     |
       | LCHIJA | enderiomachines                   | 5.3.70                              | EnderIO-1.12.2-5.3.70.jar                                   | None                                     |
       | LCHIJA | enderiopowertools                 | 5.3.70                              | EnderIO-1.12.2-5.3.70.jar                                   | None                                     |
       | LCHIJA | mcmultipart                       | 2.5.3                               | MCMultiPart-2.5.3.jar                                       | None                                     |
       | LCHIJA | mekanism                          | 1.12.2-9.8.3.390                    | Mekanism-1.12.2-9.8.3.390.jar                               | None                                     |
       | LCHIJA | gasconduits                       | 5.3.70                              | EnderIO-conduits-mekanism-1.12.2-5.3.70.jar                 | None                                     |
       | LCHIJA | enderioendergy                    | 5.3.70                              | EnderIO-endergy-1.12.2-5.3.70.jar                           | None                                     |
       | LCHIJA | enderstorage                      | 2.4.6.137                           | EnderStorage-1.12.2-2.4.6.137-universal.jar                 | f1850c39b2516232a2108a7bd84d1cb5df93b261 |
       | LCHIJA | enderutilities                    | 0.7.15                              | enderutilities-1.12.2-0.7.15.jar                            | 2b03e1423915a189b8094816baa18f239d576dff |
       | LCHIJA | erebus                            | 1.0.32                              | Erebus-1.0.32.jar                                           | None                                     |
       | LCHIJA | erebusfix                         | 1.12.2-0.0.0.1                      | erebusfix-1.12.2-0.0.0.1.jar                                | None                                     |
       | LCHIJA | evilcraft                         | 0.10.78                             | EvilCraft-1.12.2-0.10.78.jar                                | bd0353b3e8a2810d60dd584e256e364bc3bedd44 |
       | LCHIJA | evilcraftcompat                   | 1.0.0                               | EvilCraft-1.12.2-0.10.78.jar                                | None                                     |
       | LCHIJA | extendedcrafting                  | 1.7.0                               | ExtendedCrafting-Nomifactory-Edition-1.7.0.jar              | None                                     |
       | LCHIJA | extracells                        | 2.6.7                               | ExtraCells-1.12.2-2.6.7.jar                                 | None                                     |
       | LCHIJA | extracpus                         | 1.12.2-1.2.1                        | extracpus-1.12.2-1.2.1.jar                                  | None                                     |
       | LCHIJA | extrautils2                       | 1.0                                 | extrautils2-1.12-1.9.9.jar                                  | None                                     |
       | LCHIJA | zerocore                          | 1.12.2-0.1.2.9                      | zerocore-1.12.2-0.1.2.9.jar                                 | None                                     |
       | LCHIJA | bigreactors                       | 1.12.2-0.4.5.68                     | ExtremeReactors-1.12.2-0.4.5.68.jar                         | None                                     |
       | LCHIJA | foamfix                           | @VERSION@                           | foamfix-0.10.15-1.12.2.jar                                  | None                                     |
       | LCHIJA | forgemultipartcbe                 | 2.6.2.83                            | ForgeMultipart-1.12.2-2.6.2.83-universal.jar                | f1850c39b2516232a2108a7bd84d1cb5df93b261 |
       | LCHIJA | microblockcbe                     | 2.6.2.83                            | ForgeMultipart-1.12.2-2.6.2.83-universal.jar                | None                                     |
       | LCHIJA | minecraftmultipartcbe             | 2.6.2.83                            | ForgeMultipart-1.12.2-2.6.2.83-universal.jar                | None                                     |
       | LCHIJA | forgivingvoid                     | 1.1.0                               | ForgivingVoid_1.12.2-1.1.0.jar                              | None                                     |
       | LCHIJA | storagedrawers                    | 5.2.2                               | StorageDrawers-1.12.2-5.4.2.jar                             | None                                     |
       | LCHIJA | framedcompactdrawers              | 1.2.7                               | framedcompactdrawers-1.2.7.jar                              | None                                     |
       | LCHIJA | ftbbackups                        | 1.1.0.1                             | FTBBackups-1.1.0.1.jar                                      | None                                     |
       | LCHIJA | ftbutilities                      | 5.4.1.131                           | FTBUtilities-5.4.1.131.jar                                  | None                                     |
       | LCHIJA | galacticraftcore                  | 4.0.2.280                           | GalacticraftCore-1.12.2-4.0.2.280.jar                       | None                                     |
       | LCHIJA | galacticraftplanets               | 4.0.2.280                           | Galacticraft-Planets-1.12.2-4.0.2.280.jar                   | None                                     |
       | LCHIJA | galacticrafttweaker               | 1.12.2-1.0.3                        | GalacticraftTweaker-1.12.2-1.0.3.jar                        | b02331787272ec3515ebe63ecdeea0d746653468 |
       | LCHIJA | gbook                             | 2.9.5                               | Guidebook-1.12.2-2.9.5.jar                                  | None                                     |
       | LCHIJA | hammercore                        | 2.0.6.32                            | HammerLib-1.12.2-2.0.6.32.jar                               | 9f5e2a811a8332a842b34f6967b7db0ac4f24856 |
       | LCHIJA | teslacorelib                      | 1.0.18                              | tesla-core-lib-1.12.2-1.0.18.jar                            | d476d1b22b218a10d845928d1665d45fce301b27 |
       | LCHIJA | industrialforegoing               | 1.12.2-1.12.2                       | industrialforegoing-1.12.2-1.12.13-237.jar                  | None                                     |
       | LCHIJA | initialinventory                  | 2.0.2                               | InitialInventory-3.0.0.jar                                  | None                                     |
       | LCHIJA | integrateddynamics                | 1.1.11                              | IntegratedDynamics-1.12.2-1.1.11.jar                        | bd0353b3e8a2810d60dd584e256e364bc3bedd44 |
       | LCHIJA | integrateddynamicscompat          | 1.0.0                               | IntegratedDynamics-1.12.2-1.1.11.jar                        | None                                     |
       | LCHIJA | integratedtunnels                 | 1.6.14                              | IntegratedTunnels-1.12.2-1.6.14.jar                         | bd0353b3e8a2810d60dd584e256e364bc3bedd44 |
       | LCHIJA | integratedtunnelscompat           | 1.0.0                               | IntegratedTunnels-1.12.2-1.6.14.jar                         | None                                     |
       | LCHIJA | inventorytweaks                   | 1.63+release.109.220f184            | InventoryTweaks-1.63.jar                                    | 55d2cd4f5f0961410bf7b91ef6c6bf00a766dcbe |
       | LCHIJA | inworldcrafting                   | 1.12.2-1.2.0                        | inworldcrafting-1.12.2-1.2.0-universal.jar                  | None                                     |
       | LCHIJA | ironchest                         | 1.12.2-7.0.67.844                   | ironchest-1.12.2-7.0.72.847.jar                             | None                                     |
       | LCHIJA | jeiutilities                      | 0.2.9                               | JEI-Utilities-1.12.2-0.2.9.jar                              | None                                     |
       | LCHIJA | jetif                             | 1.5.2                               | jetif-1.12.2-1.5.2.jar                                      | None                                     |
       | LCHIJA | jecalculation                     | 1.12.2-3.2.7                        | JustEnoughCalculation-1.12.2-3.2.7.jar                      | None                                     |
       | LCHIJA | justenoughreactors                | 1.1.3.61                            | JustEnoughReactors-1.12.2-1.1.3.61.jar                      | 2238d4a92d81ab407741a2fdb741cebddfeacba6 |
       | LCHIJA | loottweaker                       | 0.3.1                               | LootTweaker-0.3.1+MC1.12.2.jar                              | None                                     |
       | LCHIJA | jeresources                       | 0.9.2.60                            | JustEnoughResources-1.12.2-0.9.2.60.jar                     | None                                     |
       | LCHIJA | knowledgeshare                    | 1.1                                 | knowledgeshare-1.1.jar                                      | None                                     |
       | LCHIJA | laggoggles                        | 1.12.2-5.8-132                      | LagGoggles-1.12.2-5.8-132.jar                               | None                                     |
       | LCHIJA | lightningcraft                    | 2.9.7_1                             | lightningcraft-2.9.7_1.jar                                  | None                                     |
       | LCHIJA | mysticalagriculture               | 1.7.5                               | MysticalAgriculture-1.12.2-1.7.5.jar                        | None                                     |
       | LCHIJA | matc                              | 1.0.1-hotfix                        | matc-1.0.1-hotfix.jar                                       | None                                     |
       | LCHIJA | mcjtylib_ng                       | 3.5.4                               | mcjtylib-1.12-3.5.4.jar                                     | None                                     |
       | LCHIJA | mjrlegendslib                     | 1.12.2-1.2.1                        | MJRLegendsLib-1.12.2-1.2.1.jar                              | b02331787272ec3515ebe63ecdeea0d746653468 |
       | LCHIJA | testdummy                         | 1.12                                | MmmMmmMmmMmm-1.12-1.14.jar                                  | None                                     |
       | LCHIJA | moartinkers                       | 0.6.0                               | moartinkers-0.6.0.jar                                       | None                                     |
       | LCHIJA | mob_grinding_utils                | 0.3.13                              | MobGrindingUtils-0.3.13.jar                                 | None                                     |
       | LCHIJA | modularmachinery                  | 1.10.0                              | modularmachinery-1.12.2-1.10.0.jar                          | a0f0b759d895c15ceb3e3bcb5f3c2db7c582edf0 |
       | LCHIJA | modulardiversity                  | 1.8                                 | Modular Diversity-1.8.jar                                   | None                                     |
       | LCHIJA | modularmagic                      | 1.4.0                               | modularmagic-1.4.0.jar                                      | None                                     |
       | LCHIJA | moreoverlays                      | 1.15.1                              | moreoverlays-1.15.1-mc1.12.2.jar                            | None                                     |
       | LCHIJA | moretweaker                       | 1.0.19                              | MoreTweaker-1.0.19.jar                                      | None                                     |
       | LCHIJA | morpheus                          | 1.12.2-3.5.106                      | Morpheus-1.12.2-3.5.106.jar                                 | None                                     |
       | LCHIJA | mputils                           | 1.5.6                               | MPUtils-1.12.2-1.5.7.jar                                    | None                                     |
       | LCHIJA | mpbasic                           | 1.4.7                               | mpbasic-1.12.2-1.4.11.jar                                   | None                                     |
       | LCHIJA | mrtjpcore                         | 2.1.4.43                            | MrTJPCore-1.12.2-2.1.4.43-universal.jar                     | None                                     |
       | LCHIJA | mymworlddownloader                | 1.12.2-2.2.1                        | MyM-WorldDownloader-client-1.12.2-2.2.1-all.jar             | None                                     |
       | LCHIJA | mymcosmetics                      | 1.0                                 | MyMCosmetics-client-1.12.2-1.0-all.jar                      | None                                     |
       | LCHIJA | mysticalagradditions              | 1.3.2                               | MysticalAgradditions-1.12.2-1.3.2.jar                       | None                                     |
       | LCHIJA | immersiveengineering              | 0.12-98                             | ImmersiveEngineering-0.12-98.jar                            | None                                     |
       | LCHIJA | mystagradcompat                   | 1.2                                 | mystagradcompat-1.2.jar                                     | None                                     |
       | LCHIJA | natura                            | 1.12.2-4.3.2.69                     | natura-1.12.2-4.3.2.69.jar                                  | None                                     |
       | LCHIJA | neat                              | 1.4-17                              | Neat 1.4-17.jar                                             | None                                     |
       | LCHIJA | neenergistics                     | 2.0.1                               | NotEnoughEnergistics-1.12.2-2.0.1.jar                       | None                                     |
       | LCHIJA | neid                              | 1.5.4.4                             | NotEnoughIDs-1.5.4.4.jar                                    | None                                     |
       | LCHIJA | oauth                             | 1.06.4                              | oauth-1.06.4.jar                                            | None                                     |
       | LCHIJA | openmods                          | 0.12.2                              | OpenModsLib-1.12.2-0.12.2.jar                               | d2a9a8e8440196e26a268d1f3ddc01b2e9c572a5 |
       | LCHIJA | openblocks                        | 1.8.1                               | OpenBlocks-1.12.2-1.8.1.jar                                 | d2a9a8e8440196e26a268d1f3ddc01b2e9c572a5 |
       | LCHIJA | oreexcavation                     | 1.4.150                             | OreExcavation-1.4.150.jar                                   | None                                     |
       | LCHIJA | packagedauto                      | 1.12.2-1.0.5.19                     | PackagedAuto-1.12.2-1.0.5.19.jar                            | None                                     |
       | LCHIJA | placebo                           | 1.6.0                               | Placebo-1.12.2-1.6.0.jar                                    | None                                     |
       | LCHIJA | planefix                          | 1.0.0                               | PlaneFix-1.12.2-1.0.0.jar                                   | None                                     |
       | LCHIJA | planetprogression                 | 1.12.2-0.4.8                        | PlanetProgression-1.12.2-0.4.8.jar                          | b02331787272ec3515ebe63ecdeea0d746653468 |
       | LCHIJA | projectred-core                   | 4.9.4.120                           | ProjectRed-1.12.2-4.9.4.120-Base.jar                        | None                                     |
       | LCHIJA | thermaldynamics                   | 2.5.6                               | ThermalDynamics-1.12.2-2.5.6.1-universal.jar                | None                                     |
       | LCHIJA | simplyjetpacks                    | 1.12.2-2.2.20.0                     | SimplyJetpacks2-1.12.2-2.2.20.0.jar                         | None                                     |
       | LCHIJA | plustic                           | @VERSION@                           | plustic-8.0.3.jar                                           | None                                     |
       | LCHIJA | projectintelligence               | 1.0.9                               | ProjectIntelligence-1.12.2-1.0.9.28-universal.jar           | None                                     |
       | LCHIJA | projectred-integration            | 4.9.4.120                           | ProjectRed-1.12.2-4.9.4.120-integration.jar                 | None                                     |
       | LCHIJA | projectred-transmission           | 4.9.4.120                           | ProjectRed-1.12.2-4.9.4.120-integration.jar                 | None                                     |
       | LCHIJA | quantumflux                       | 2.0.18                              | quantumflux-1.12.2-2.0.18.jar                               | None                                     |
       | LCHIJA | reborncore                        | 3.19.5                              | RebornCore-1.12.2-3.19.5-universal.jar                      | None                                     |
       | LCHIJA | reccomplex                        | 1.4.8.2                             | RecurrentComplex-1.4.8.2.jar                                | None                                     |
       | LCHIJA | requious                          | 1.0                                 | Requious Frakto-0.12.jar                                    | None                                     |
       | LCHIJA | resourceloader                    | 1.5.3                               | ResourceLoader-MC1.12.1-1.5.3.jar                           | d72e0dd57935b3e9476212aea0c0df352dd76291 |
       | LCHIJA | restrictedportals                 | 1.12-0.6.3                          | restrictedportals-1.12-0.6.3.jar                            | None                                     |
       | LCHIJA | rftools                           | 7.73                                | rftools-1.12-7.73.jar                                       | None                                     |
       | LCHIJA | rftoolsdim                        | 5.71                                | rftoolsdim-1.12-5.71.jar                                    | None                                     |
       | LCHIJA | roots                             | @VERSION@                           | Roots-1.12.2-3.1.6.jar                                      | None                                     |
       | LCHIJA | ruins                             | 17.2                                | Ruins-1.12.2.jar                                            | None                                     |
       | LCHIJA | simplevoidworld                   | 1.2.0.9                             | Simple-Void-World-1.12-1.2.0.9-universal.jar                | None                                     |
       | LCHIJA | simpleautorun                     | 1.12.1-1.2                          | simpleautorun-1.12.2-1.2.0.jar                              | None                                     |
       | LCHIJA | simple_trophies                   | 1.2.2                               | simpletrophies-1.2.2.1.jar                                  | None                                     |
       | LCHIJA | simplybackpacks                   | 1.4.9                               | simplybackpacks-1.4.9.jar                                   | None                                     |
       | LCHIJA | solarflux                         | 12.4.11                             | SolarFluxReborn-1.12.2-12.4.11.jar                          | 9f5e2a811a8332a842b34f6967b7db0ac4f24856 |
       | LCHIJA | spark                             | 1.6.3                               | spark-forge.jar                                             | None                                     |
       | LCHIJA | spartanshields                    | 1.5.5                               | SpartanShields-1.12.2-1.5.5.jar                             | None                                     |
       | LCHIJA | bq_standard                       | 3.4.173                             | StandardExpansion-3.4.173.jar                               | None                                     |
       | LCHIJA | storagedrawersextra               | @VERSION@                           | StorageDrawersExtras-1.12-3.1.0.jar                         | None                                     |
       | LCHIJA | supersoundmuffler                 | 1.0.2.10                            | supersoundmuffler-revived_1.12.2_1.0.2.10.jar               | None                                     |
       | LCHIJA | texfix                            | 4.0                                 | TexFix+V-1.12-4.0.jar                                       | None                                     |
       | LCHIJA | thaumicaugmentation               | 1.12.2-2.1.8                        | ThaumicAugmentation-1.12.2-2.1.8.jar                        | 8f678591ba6f78d579e553a8aa94b4c4766cb13d |
       | LCHIJA | thaumicjei                        | 1.6.0                               | ThaumicJEI-1.12.2-1.6.0-27.jar                              | None                                     |
       | LCHIJA | thaumicenergistics                | 2.2.5                               | thaumicenergistics-2.2.5.jar                                | None                                     |
       | LCHIJA | tcinventoryscan                   | 2.0.10                              | ThaumicInventoryScanning_1.12.2-2.0.10.jar                  | None                                     |
       | LCHIJA | tinkersaddons                     | 1.0.7                               | Tinkers' Addons-1.12.1-1.0.7.jar                            | None                                     |
       | LCHIJA | tinkersaether                     | 1.4.1                               | tinkersaether-1.4.1.jar                                     | None                                     |
       | LCHIJA | tinkersjei                        | 1.2                                 | tinkersjei-1.2.jar                                          | None                                     |
       | LCHIJA | tinkersoredictcache               | 1.0                                 | TinkersOreDictCache-1.0.jar                                 | None                                     |
       | LCHIJA | tips                              | 1.0.9                               | Tips-1.12.2-1.0.9.jar                                       | d476d1b22b218a10d845928d1665d45fce301b27 |
       | LCHIJA | tipthescales                      | 1.0.4                               | TipTheScales-1.12.2-1.0.4.jar                               | None                                     |
       | LCHIJA | tmel                              | 1.12.2-1.4.0.0                      | tmel-1.12.2-1.4.0.0.jar                                     | None                                     |
       | LCHIJA | toastcontrol                      | 1.8.1                               | Toast Control-1.12.2-1.8.1.jar                              | None                                     |
       | LCHIJA | tombmanygraves                    | 1.12-4.2.0                          | TombManyGraves-1.12-4.2.0.jar                               | None                                     |
       | LCHIJA | torchmaster                       | 1.8.5.0                             | torchmaster_1.12.2-1.8.5.0.jar                              | None                                     |
       | LCHIJA | totemic                           | 1.12.2-0.11.6                       | Totemic-1.12.2-0.11.6.jar                                   | 21d11d7bf4d97b465382a1f95428029aac6daaea |
       | LCHIJA | traverse                          | 1.6.0                               | Traverse-1.12.2-1.6.0-69.jar                                | None                                     |
       | LCHIJA | triumph                           | 3.19.2                              | Triumph-1.12.2-3.19.2.jar                                   | None                                     |
       | LCHIJA | undergroundbiomes                 | 1.3.14                              | UndergroundBiomesConstructs-1.12-1.3.14.jar                 | None                                     |
       | LCHIJA | universaltweaks                   | 1.12.2-1.2.0                        | UniversalTweaks-1.12.2-1.2.0.jar                            | None                                     |
       | LCHIJA | valkyrielib                       | 1.12.2-2.0.20.1                     | valkyrielib-1.12.2-2.0.20.1.jar                             | None                                     |
       | LCHIJA | universalmodifiers                | 1.12.2-1.0.16.1                     | valkyrielib-1.12.2-2.0.20.1.jar                             | None                                     |
       | LCHIJA | vanillafix                        | 1.0.10-150                          | VanillaFix-1.0.10-150.jar                                   | None                                     |
       | LCHIJA | vtb                               | 2.0.0                               | VillagerTradingBan-2.0.0.6-universal.jar                    | None                                     |
       | LCHIJA | wailaharvestability               | 1.1.12                              | WailaHarvestability-mc1.12-1.1.12.jar                       | None                                     |
       | LCHIJA | wawla                             | 2.6.275                             | Wawla-1.12.2-2.6.275.jar                                    | d476d1b22b218a10d845928d1665d45fce301b27 |
       | LCHIJA | wct                               | 3.12.97                             | WirelessCraftingTerminal-1.12.2-3.12.97.jar                 | 186bc454cd122c9c2f1aa4f95611254bcc543363 |
       | LCHIJA | wft                               | 1.0.4                               | WirelessFluidTerminal-1.12.2-1.0.4.jar                      | 186bc454cd122c9c2f1aa4f95611254bcc543363 |
       | LCHIJA | worldeditcuife3                   | 3.0.5                               | WorldEdit-CUI-FE3-1.12.2-3.0.5.jar                          | None                                     |
       | LCHIJA | wrcbe                             | 2.3.2                               | WR-CBE-1.12.2-2.3.2.33-universal.jar                        | f1850c39b2516232a2108a7bd84d1cb5df93b261 |
       | LCHIJA | zenutils                          | 1.12.2                              | zenutils-1.12.2.jar                                         | None                                     |
       | LCHIJA | mysticallib                       | 1.12.2-1.13.0                       | mysticallib-1.12.2-1.13.0.jar                               | None                                     |
       | LCHIJA | teslacorelib_registries           | 1.0.18                              | tesla-core-lib-1.12.2-1.0.18.jar                            | None                                     |
       | LCHIJA | tweakersconstructpostload         | 1.12.2-1.6.1                        | tweakersconstruct-1.12.2-1.6.1.jar                          | None                                     |
       | LCHIJA | unidict                           | 1.12.2-3.0.10                       | UniDict-1.12.2-3.0.10.jar                                   | None                                     |
  Loaded coremods (and transformers): IELoadingPlugin (ImmersiveEngineering-core-0.12-98.jar)
                                        blusunrize.immersiveengineering.common.asm.IEClassTransformer
                                      MekanismCoremod (Mekanism-1.12.2-9.8.3.390.jar)
                                        mekanism.coremod.KeybindingMigrationHelper
                                      MicdoodlePlugin (MicdoodleCore-1.12.2-4.0.2.280.jar)
                                        micdoodle8.mods.miccore.MicdoodleTransformer
                                      BewitchmentFMLLoadingPlugin (bewitchment-1.12.2-0.0.22.64.jar)
                                        
                                      Quark Plugin (Quark-r1.6-179.jar)
                                        vazkii.quark.base.asm.ClassTransformer
                                      TickCentral (TickCentral-3.2.jar)
                                        com.github.terminatornl.laggoggles.tickcentral.EventBusTransformer
                                        com.github.terminatornl.laggoggles.tickcentral.RenderManagerTransformer
                                        com.github.terminatornl.tickcentral.asm.BlockTransformer
                                        com.github.terminatornl.tickcentral.asm.ITickableTransformer
                                        com.github.terminatornl.tickcentral.asm.EntityTransformer
                                        com.github.terminatornl.tickcentral.asm.HubAPITransformer
                                      UniDictCoreMod (UniDict-1.12.2-3.0.10.jar)
                                        wanion.unidict.core.UniDictCoreModTransformer
                                      Inventory Tweaks Coremod (InventoryTweaks-1.63.jar)
                                        invtweaks.forge.asm.ContainerTransformer
                                      EnderCorePlugin (EnderCore-1.12.2-0.5.76-core.jar)
                                        com.enderio.core.common.transform.EnderCoreTransformer
                                        com.enderio.core.common.transform.SimpleMixinPatcher
                                      Thaumic Augmentation Core Plugin (ThaumicAugmentation-1.12.2-2.1.8.jar)
                                        thecodex6824.thaumicaugmentation.core.TATransformer
                                      NEELoadingPlugin (NotEnoughEnergistics-1.12.2-2.0.1.jar)
                                        com.github.vfyjxf.nee.asm.NEEClassTransformer
                                      AE2ELCore (appliedenergistics2-rv6-stable-7-extended_life-v0.54.19.jar)
                                        appeng.core.transformer.AE2ELTransformer
                                      LoadingPlugin (ResourceLoader-MC1.12.1-1.5.3.jar)
                                        lumien.resourceloader.asm.ClassTransformer
                                      ToolProgressionPlugin (toolprogression-core-1.12.2-1.6.12.jar)
                                        tyra314.toolprogression.core.asm.ToolProgressionClassTransformer
                                      IvToolkit (IvToolkit-1.3.3-1.12.jar)
                                        
                                      UniversalTweaksCore (UniversalTweaks-1.12.2-1.2.0.jar)
                                        
                                      MixinBooter (!mixinbooter-7.0.jar)
                                        
                                      ErebusFix Mixin Loading Plugin (erebusfix-1.12.2-0.0.0.1.jar)
                                        
                                      RandomPatches (randompatches-1.12.2-1.22.1.10.jar)
                                        com.therandomlabs.randompatches.core.RPTransformer
                                      Do not report to Forge! (If you haven't disabled the FoamFix coremod, try disabling it in the config! Note that this bit of text will still appear.) (foamfix-0.10.15-1.12.2.jar)
                                        pl.asie.foamfix.coremod.FoamFixTransformer
                                      BedPatch (bedpatch-2.2-1.12.2.jar)
                                        com.mordenkainen.bedpatch.BedPatchASM
                                      ForgelinPlugin (Forgelin-1.8.4.jar)
                                        
                                      DupeFixProjectCoreMod (DupeFixProject-1.12.2-3.1.6.jar)
                                        
                                      OpenModsCorePlugin (OpenModsLib-1.12.2-0.12.2.jar)
                                        openmods.core.OpenModsClassTransformer
                                      Ar_CorePlugin (additionalresources-1.9.4-0.2.0.28+47cd0bd_signed.jar)
                                        
                                      CTMCorePlugin (CTM-MC1.12.2-1.0.2.31.jar)
                                        team.chisel.ctm.client.asm.CTMTransformer
                                      Plugin (NotEnoughIDs-1.5.4.4.jar)
                                        ru.fewizz.neid.asm.Transformer
                                      BNBGamingCore (BNBGamingCore-1.12.2-0.12.0.jar)
                                        com.bloodnbonesgaming.bnbgamingcore.core.BNBGamingCoreClassTransformer
                                      AstralCore (astralsorcery-1.12.2-1.10.27.jar)
                                        
                                      VanillaFixLoadingPlugin (VanillaFix-1.0.10-150.jar)
                                        
                                      CreativePatchingLoader (CreativeCore_v1.9.19_mc1.12.2.jar)
                                        
                                      AstralLevelNerfPlugin (astral-level-nerf-1.0.1-all.jar)
                                        mixu.astrallevelnerf.asm.AstralLevelNerfTransformer
                                      HCASM (HammerLib-1.12.2-2.0.6.32.jar)
                                        com.zeitheron.hammercore.asm.HammerCoreTransformer
                                      ItemPatchingLoader (ItemPhysic+Lite+1.3.7+mc1.12.2.jar)
                                        com.creativemd.itemphysic.ItemTransformer
                                      JeiUtilitiesLoadingPlugin (JEI-Utilities-1.12.2-0.2.9.jar)
                                        com.github.vfyjxf.jeiutilities.asm.JeiUtilitiesClassTransformer
  GL info: ' Vendor: 'NVIDIA Corporation' Version: '4.6.0 NVIDIA 527.56' Renderer: 'NVIDIA GeForce GTX 1650/PCIe/SSE2'
  OpenModsLib class transformers: [llama_null_fix:FINISHED],[horse_base_null_fix:FINISHED],[pre_world_render_hook:FINISHED],[player_render_hook:FINISHED],[horse_null_fix:FINISHED]
  Ender IO: No known problems detected.
            Authlib is : /C:/Users/kshar/AppData/Roaming/.mineyourmind/libraries/com/mojang/authlib/1.5.25/authlib-1.5.25.jar
            
            !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!
            !!!You are looking at the diagnostics information, not at the crash.       !!!
            !!!Scroll up until you see the line with '---- Minecraft Crash Report ----'!!!
            !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!
  Pulsar/tconstruct loaded Pulses: - TinkerCommons (Enabled/Forced)
                                   - TinkerWorld (Enabled/Not Forced)
                                   - TinkerTools (Enabled/Not Forced)
                                   - TinkerHarvestTools (Enabled/Forced)
                                   - TinkerMeleeWeapons (Enabled/Forced)
                                   - TinkerRangedWeapons (Enabled/Forced)
                                   - TinkerModifiers (Enabled/Forced)
                                   - TinkerSmeltery (Enabled/Not Forced)
                                   - TinkerGadgets (Enabled/Not Forced)
                                   - TinkerOredict (Enabled/Forced)
                                   - TinkerIntegration (Enabled/Forced)
                                   - TinkerFluids (Enabled/Forced)
                                   - TinkerMaterials (Enabled/Forced)
                                   - TinkerModelRegister (Enabled/Forced)
                                   - chiselIntegration (Enabled/Not Forced)
                                   - chiselsandbitsIntegration (Enabled/Not Forced)
                                   - craftingtweaksIntegration (Enabled/Not Forced)
                                   - wailaIntegration (Enabled/Not Forced)
                                   - quarkIntegration (Enabled/Not Forced)
  AE2 Version: stable rv6-stable-7-extended_life-v0.54.19 for Forge 14.23.5.2847
  HammerCore Debug Information: Dependent Mods: None.
  Pulsar/natura loaded Pulses: - NaturaCommons (Enabled/Forced)
                               - NaturaOverworld (Enabled/Not Forced)
                               - NaturaNether (Enabled/Not Forced)
                               - NaturaDecorative (Enabled/Not Forced)
                               - NaturaTools (Enabled/Not Forced)
                               - NaturaEntities (Enabled/Not Forced)
                               - NaturaOredict (Enabled/Forced)
                               - NaturaWorld (Enabled/Not Forced)
                               - craftingtweaksIntegration (Enabled/Not Forced)
  Patchouli open book context: n/a
  Extended Crafting: Nomifactory Edition: You are using a fork of Extended Crafting created for the Nomifactory modpack.
                                          If the error above is a NoSuchFieldError or a NoSuchMethodError relating to
                                          com.blakebr0.extendedcrafting,
                                          then please report to https://github.com/Nomifactory/ExtendedCrafting/issues
                                          with this crash report.
                                          Otherwise, you can ignore this message.
  RebornCore: Plugin Engine: 0
              RebornCore Version: 3.19.5
              Runtime Debofucsation 1
              Invalid fingerprint detected for RebornCore!
              RenderEngine: 0
  AE2 Integration: IC2:OFF, GTCE:OFF, RC:OFF, MFR:OFF, Waila:ON, InvTweaks:ON, JEI:ON, Mekanism:ON, OpenComputers:OFF, THE_ONE_PROBE:OFF, TESLA:OFF, CRAFTTWEAKER:ON
  Suspected Mods: Immersive Engineering (immersiveengineering), TickCentral (tickcentral), Hammer Core (hammercore)
  Launched Version: 1.12.2
  LWJGL: 2.9.4
  OpenGL: NVIDIA GeForce GTX 1650/PCIe/SSE2 GL version 4.6.0 NVIDIA 527.56, NVIDIA Corporation
  GL Caps: Using GL 1.3 multitexturing.
           Using GL 1.3 texture combiners.
           Using framebuffer objects because OpenGL 3.0 is supported and separate blending is supported.
           Shaders are available because OpenGL 2.1 is supported.
           VBOs are available because OpenGL 1.5 is supported.
  Using VBOs: Yes
  Is Modded: Definitely; Client brand changed to 'fml,forge'
  Type: Client (map_client.txt)
  Resource Packs: 
  Current Language: English (US)
  Profiler Position: N/A (disabled)
  CPU: 12x AMD Ryzen 5 4600H with Radeon Graphics
  Client Crashes Since Restart: 3
  Integrated Server Crashes Since Restart: 0
