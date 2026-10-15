# Call of Duty RPCN configs for PS5SX3

Settings for playing **Call of Duty** games online through **RPCN**, RPCS3's replacement for PSN, on **PS5SX3**, the PS3 emulator for PS5. PS5SX3 has no Network settings screen, so these files set it up for each game.

## What works online

From the RPCS3 wiki's [RPCN Compatibility List](https://wiki.rpcs3.net/index.php?title=RPCN_Compatibility_List):

| Game | Online through RPCN |
|---|---|
| Call of Duty Classic | **Works**: connects, lobbies and matches |
| Call of Duty: World at War | **Works** on update 1.07, through a community server (its DNS is set in these files) |
| Call of Duty 4: Modern Warfare | Does not connect: no community server yet |
| Call of Duty: Modern Warfare 2 | Does not connect: no community server yet |
| Call of Duty: Modern Warfare 3 | Not tested yet |
| Call of Duty: Black Ops | Does not connect: no community server yet |
| Call of Duty: Black Ops II | Does not connect: no community server yet |
| Call of Duty: Black Ops III | Does not connect: no community server yet |
| Call of Duty: Ghosts | Does not connect: no community server yet |
| Call of Duty: Ghosts Multiplayer Demo | Not tested yet |
| Call of Duty: Advanced Warfare | Does not connect: no community server yet |

The games that don't connect still sign in to RPCN, but their online modes have no server to talk to. If a community server appears for one of them, only the `DNS address` line in its files needs to change.

## Install

1. Copy the files from this repo's `game_configs` folder into the `game_configs` folder of PS5SX3 (next to its `eboot.bin`). They have to go directly in that folder, not in a subfolder. You only need the files for the title IDs you own, but copying all of them is fine. If PS5SX3 already has a file with the same name, add the `Net:` section to that file instead of replacing it.
2. In PS5SX3, sign in to RPCN on the official RPCN server.
3. Start the game.

## What the files set

Each `config_<title ID>.yml` changes only network settings. PS5SX3's launcher merges them with its own settings for the game.

| Setting | Value |
|---|---|
| Internet enabled | Connected |
| PSN status | RPCN |
| DNS address | 8.8.8.8 (World at War: 67.222.156.250, its community server) |
| UPNP Enabled | On, so RPCS3 can ask your router to open the game's ports (UDP 3074) |

## Title IDs

| Game | Title IDs |
|---|---|
| Call of Duty Classic | NPEB00101, NPEB00113, NPUB30065 |
| Call of Duty: World at War | BLES00354, BLES00355, BLES00357, BLES00404, BLES00457, BLKS20098, BLUS30192 |
| Call of Duty 4: Modern Warfare | BLES00148, BLES00149, BLES00155, BLJS10013, BLKS20048, BLUS30072, NPEB00740, NPUB30588 |
| Call of Duty: Modern Warfare 2 | BLES00683, BLES00685, BLES00687, BLES00690, BLES00691, BLJM60191, BLUS30377, BLUS30429, NPEB00731, NPUB30585 |
| Call of Duty: Modern Warfare 3 | BLES01428, BLES01430, BLES01431, BLES01432, BLES01433, BLES01434, BLJM60404, BLUS30838, NPUB30787 |
| Call of Duty: Black Ops | BLES01031, BLES01032, BLES01033, BLES01034, BLES01035, BLES01105, BLJM60286, BLJM60287, BLUS30591, NPEB00756, NPUB30584 |
| Call of Duty: Black Ops II | BLES01717, BLES01718, BLES01719, BLES01720, BLUS31011, BLUS31140, NPUB31054 |
| Call of Duty: Black Ops III | BLES02166, BLUS31527, NPEB02266, NPUB31665 |
| Call of Duty: Ghosts | BLES01945, BLES01948, BLJM61126, BLUS31270, NPEB01832, NPEB01835, NPUB31301 |
| Call of Duty: Ghosts Multiplayer Demo | NPEB90534, NPUB91004 |
| Call of Duty: Advanced Warfare | BLES02077, BLES02078, BLUS31466, NPEB02087, NPEB02088, NPUB31553 |

## Sources

- RPCS3 wiki: [Help:Netplay](https://wiki.rpcs3.net/index.php?title=Help:Netplay) and the [RPCN Compatibility List](https://wiki.rpcs3.net/index.php?title=RPCN_Compatibility_List)
- [RPCN Browser](https://rpcs3.net/rpcn), the list of games played through RPCN
- World at War's community server: [JOFFY's setup video](https://www.youtube.com/watch?v=d3bFId8nQm8)
- Title IDs: [RPCS3 compatibility database](https://rpcs3.net/compatibility?g=call+of+duty)
