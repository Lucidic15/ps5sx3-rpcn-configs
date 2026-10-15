# RPCN online configs for PS5SX3

Settings for playing PS3 games online through **RPCN**, RPCS3's replacement for PSN, on **PS5SX3**, the PS3 emulator for PS5. PS5SX3 has no Network settings screen, so these files set it up for each game.

There's one file per title ID: 1809 configs covering the 681 games on the RPCS3 wiki's [RPCN Compatibility List](https://wiki.rpcs3.net/index.php?title=RPCN_Compatibility_List), plus two Call of Duty games from the [RPCN Browser](https://rpcs3.net/rpcn). Find your game and its title IDs in [GAMES.md](GAMES.md).

## Install

1. Copy the files for your games from this repo's `game_configs` folder into the `game_configs` folder of PS5SX3 (next to its `eboot.bin`). They have to go directly in that folder, not in a subfolder. Copying all of them is fine.
2. In PS5SX3, sign in to RPCN on the official RPCN server.
3. Start the game.

If PS5SX3 already has a file with the same name, add the `Net:` section to that file instead of replacing it.

## What the files set

| Setting | Value |
|---|---|
| Internet enabled | Connected |
| PSN status | RPCN |
| DNS address | 8.8.8.8, unless the game uses a custom server's DNS (see below) |
| IP swap list | Only for games whose RPCS3 wiki page gives IP/Host switches (see below) |
| UPNP Enabled | On, so RPCS3 can ask your router to open the game's ports |

Each file also has comments with the game's results from the RPCN Compatibility List: whether it connects, makes lobbies, matches players, and has online features working.

## Games that don't use 8.8.8.8

Most games use DNS 8.8.8.8, RPCS3's default. 86 games have a fan-made custom server listed on their RPCS3 wiki page, so their files point at that server instead, through either a custom DNS or IP/Host switches.

### Custom DNS

| DNS address | Games |
|---|---|
| `146.190.205.197` | 007: Quantum of Solace, Band Hero, BlackSite: Area 51, Call of Duty 3, Colin McRae: DiRT, Far Cry 3, Ghostbusters: The Video Game, Guitar Hero 5, Guitar Hero III: Legends of Rock, Guitar Hero World Tour, Guitar Hero: Aerosmith, Guitar Hero: Metallica, Guitar Hero: Smash Hits, Guitar Hero: Van Halen, Guitar Hero: Warriors of Rock, Haze, James Bond 007: Blood Stone, James Cameron's Avatar: The Game, Operation Flashpoint: Dragon Rising, Race Driver: GRID, Shaun White Skateboarding, Shaun White Snowboarding, Singularity, Stranglehold, Stuntman: Ignition, The Club, The History Channel: Battle for the Pacific, Tom Clancy's EndWar, Tom Clancy's Ghost Recon: Advanced Warfighter 2, Tom Clancy's Ghost Recon: Future Soldier, Tom Clancy's Splinter Cell: Double Agent, Wolfenstein |
| `67.222.156.250` | Call of Duty: World at War, Killzone 2, Killzone 3, MotorStorm, MotorStorm: Apocalypse, MotorStorm: Pacific Rift, NBA 07, Resistance 2, Resistance: Fall of Man |
| `209.38.53.69` | Blur, DJ Hero, DJ Hero 2, Transformers: Dark of the Moon, Transformers: Fall of Cybertron, Transformers: Revenge of the Fallen, Transformers: Rise of the Dark Spark, Transformers: War for Cybertron |
| `185.194.142.4` | Calling All Cars, Pain, Ratchet: Deadlocked, SOCOM: U.S Navy SEALs Confrontation |
| `51.79.41.185` | Burnout Paradise, Driver: San Francisco, The Ratchet & Clank Trilogy |
| `198.100.158.95` | Starhawk, Warhawk |
| `128.140.0.23` | Medal of Honor |
| `142.171.43.167` | Metal Gear Solid 4: Guns of the Patriots |
| `192.236.168.216` | WWE 2K14 |
| `20.101.151.59` | Fuel |
| `52.86.120.101` | PlayStation: Home |
| `72.56.104.67` | Need for Speed Carbon |

### IP/Host switches

These games keep DNS 8.8.8.8 and send only the hostnames below to the custom server.

| Game | IP/Host switches |
|---|---|
| Ace Combat Infinity | `dev-wind.siliconstudio.co.jp=127.0.0.1` |
| Armored Core 4 | `ac4.sega.com=15.204.86.103 && ps3update.fromsoftware.jp=15.204.86.103` |
| Battlefield: Bad Company 2 | `theater.ps3.arcadia=152.53.15.83 && bfbc2-ps3.fesl.ea.com=152.53.15.83` |
| Buzz! Brain of... | `buzzps3.online.scee.com=57.131.197.223` |
| Buzz! Quiz Player | `buzzps3.online.scee.com=57.131.197.223` |
| Buzz! Quiz TV | `buzzps3.online.scee.com=57.131.197.223` |
| Buzz! Quiz World | `buzzps3.online.scee.com=57.131.197.223` |
| Buzz! The Ultimate Music Quiz | `buzzps3.online.scee.com=57.131.197.223` |
| Demon's Souls | `ds-eu-c.scej-online.jp=206.189.232.242 && ds-eu-g.scej-online.jp=206.189.232.242 && c.demons-souls.com=206.189.232.242 && g.demons-souls.com=206.189.232.242 && cmnap.scej-online.jp=206.189.232.242 && demons-souls.scej-online.jp=206.189.232.242` |
| Medal of Honor: Airborne | `theater.ps3.arcadia=152.53.15.83 && mohair-ps3.fesl.ea.com=152.53.15.83` |
| Mercenaries 2: World in Flames | `theater.ps3.arcadia=152.53.15.83 && mercs2-ps3.fesl.ea.com=152.53.15.83` |
| ModNation Racers | `modnation.ps3.playstationcloud.com=45.32.179.33` |
| NHL 10 | `gosredirector.ea.com=57.131.155.88` |
| NHL 11 | `gosredirector.ea.com=57.131.155.88` |
| NHL 12 | `gosredirector.ea.com=57.131.155.88` |
| NHL 13 | `gosredirector.ea.com=57.131.155.88` |
| NHL 14 | `gosredirector.ea.com=57.131.155.88` |
| NHL 15 | `gosredirector.ea.com=57.131.155.88` |
| NHL: Legacy Edition | `gosredirector.ea.com=57.131.155.88` |
| Skate 3 | `gosredirector.ea.com=172.237.109.212 && downloads.skate.online.ea.com=172.237.109.212` |
| The Lord of the Rings Conquest | `theater.ps3.arcadia=152.53.15.83 && lotr-pandemic-ps3.fesl.ea.com=152.53.15.83` |
| WipEout HD | `wipeout2048.muis.online.scee.com=147.135.213.57 && wipeout2048.online.scee.com=147.135.213.57` |

### Games with more than one server

The files use the first server the wiki lists. The others are noted in each file's comments:

- **James Cameron's Avatar: The Game:** The wiki's notes also give the switch onlineconfigservice.ubi.com=85.90.247.249 (PS3 REBORN).
- **MotorStorm:** The wiki also lists a second server, 5.161.41.41.
- **MotorStorm: Pacific Rift:** The wiki also lists 5.161.41.41 (PSORG), which needs PSORG's RPCS3 patch.
- **PlayStation: Home:** The wiki also lists 104.37.190.154 and 51.79.41.185. Home also needs a specific client build and PKG.
- **Ratchet: Deadlocked:** The wiki also lists 51.79.41.185.
- **Warhawk:** The wiki also lists 185.194.142.4.
- **WipEout HD:** The wiki also lists the same two hosts pointed at 185.194.142.4.

### Custom servers not reached through DNS

These games are listed with custom servers too, but their pages give no DNS or IP/Host switches. Most need a game patch instead, such as the OpenSpy patches in RPCS3's patch list, or a separate tool, and a few servers don't work yet. Their files keep DNS 8.8.8.8, so check each game's RPCS3 wiki page:

50 Cent: Blood on the Sand, Age of Booty, Battlefield 1943, Beijing 2008, Blacklight: Tango Down, Brothers in Arms: Hell's Highway, Bulletstorm, CellFactor: Psychokinetic Wars, Condemned 2: Bloodshot, Damnation, Dungeon Defenders, Dungeons & Dragons: Daggerdale, F.E.A.R. 2: Project Origin, Fairytale Fights, Fatal Inertia EX, Full Auto 2: Battlelines, Gotham City Impostors, Gran Turismo 5, Gran Turismo 6, Hail to the Chimp, High Stakes on the Vegas Strip: Poker Edition, Homefront, LittleBigPlanet, LittleBigPlanet 2, LittleBigPlanet 3, LittleBigPlanet Hub, LittleBigPlanet Karting, Lucha Libre AAA: Héroes del Ring, Marvel: Ultimate Alliance, Metal Gear Online, Midnight Club: Los Angeles, Monster Hunter Frontier G, Monster Madness Grave Danger, Mortal Kombat vs. DC Universe, MUD: FIM Motocross World Championship, NBA Ballers: Chosen One, Red Baron Arcade, Rock Band 3, Saints Row 2, SBK X: Superbike World Championship, Supersonic Acrobatic Rocket-Powered Battle-Cars, TimeShift, Warp

## Games PS5SX3 already ships a config for

These title IDs aren't included, so that your copy keeps PS5SX3's own fixes for them. Add these lines to the end of the existing file in PS5SX3's `game_configs` folder instead.

**Killzone 2 (BCUS98116)** uses PS Rewired's custom server:

```yaml
Net:
  Internet enabled: "Connected"
  PSN status: "RPCN"
  DNS address: "67.222.156.250"
  UPNP Enabled: true
```

**Grand Theft Auto IV (BLES00229, BLUS30127, NPEB00882, NPUB30702) and Grand Theft Auto V (BLES01807):**

```yaml
Net:
  Internet enabled: "Connected"
  PSN status: "RPCN"
  DNS address: "8.8.8.8"
  UPNP Enabled: true
```

## Not included

- **MAG** and **Yakuza 0** are on the list, but RPCS3's database has no title ID for them. For Yakuza 0 it only has the demo.

## Sources

- RPCS3 wiki: the [RPCN Compatibility List](https://wiki.rpcs3.net/index.php?title=RPCN_Compatibility_List), [Help:Netplay](https://wiki.rpcs3.net/index.php?title=Help:Netplay) and each custom-server game's page, read on 15 October 2026.
- Title IDs: [RPCS3 compatibility database](https://rpcs3.net/compatibility). PlayStation Home's ID (NPIA00005) comes from its PlayStation Store listing.
- [RPCN Browser](https://rpcs3.net/rpcn), for the Call of Duty games not on the wiki's list.
