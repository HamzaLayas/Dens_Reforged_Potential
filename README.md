# Den's Reforged Potential

Biome progression for the Forge of Potential. The mod decides how far each item can
be refined and which idol each refinement costs, and makes the Forge's odds
configurable. By default an upgrade succeeds half of the time, and a failed upgrade
only uses up the idols: the item keeps its level and never breaks.

**Required on the server and on every client.**

## Installation

Install BepInExPack Valheim and Jötunn first. The declared dependencies are BepInExPack Valheim 5.4.2333 and Jötunn 2.30.2. A mod manager can resolve the dependencies for you.

For a manual installation:

1. Close Valheim and stop the dedicated server.
2. Back up the world, characters, and BepInEx configuration.
3. Download the installer ZIP from [Releases](https://github.com/HamzaLayas/Dens_Reforged_Potential/releases). GitHub's automatic source archives are documentation, not installers.
4. Extract the manual installer into the Valheim installation or mod-manager profile root. Its DLL belongs under `BepInEx/plugins/Dens_Reforged_Potential/`.
5. Remove older duplicate copies of `Dens_Reforged_Potential.dll` and remove `Akuichi-ReforgedPotential` before starting. Do not run both mods together.
6. Install the same version and dependencies on the server and every player's PC. Start once to generate the configuration file.

Get help and report problems at the [public player repository](https://github.com/HamzaLayas/Dens_Reforged_Potential). See the [FAQ](https://github.com/HamzaLayas/Dens_Reforged_Potential/blob/main/FAQ.md) for common questions.

## How it works

- Every idol belongs to a biome: Wooden (Meadows), Bronze (Black Forest), Iron
  (Swamp), Silver (Mountain), Black Metal (Plains), Black Marble (Mistlands),
  Flametal (Ashlands), Bloodgold (Deep North).
- An item belongs to the biome of its crafting materials.
- Each biome above an item's own adds one band of levels (3 for most gear, 2 for
  shields), unlocked when the previous biome's boss is defeated (world progress by
  default). Refining into a band costs that biome's idol.
- Armor and shields cannot outgrow the best vanilla item of their own class, so light
  armor stays light and bucklers stay bucklers.
- Gear from a biome you have not unlocked, and Deep North gear, stays at its normal
  maximum quality.
- Forge rolls are seeded from the character's random ID instead of its name, so a
  character name can no longer be picked to win an upgrade. Outcomes stay fixed per
  character, so reloading does not change them.
- Idols are crafted from their biome's materials (Workbench, Forge, Black Forge) and
  no longer appear in chests, creature drops or trader stock. Chests filled before
  installing keep their contents.

The Forge shows the next idol and the current limit. Use `drp_explain` at the Forge
for details, or `drp_catalog` to list every item.

## Configuration

`BepInEx/config/com.sterbenden.densreforgedpotential.cfg`, synced from the server
when **Enable Server Sync** is on:

- **Upgrade Settings**: Upgrade Chance (0.5), Consume Idols Only On Failure (on),
  Break Chance (1, used when the previous setting is off: the share of failures that
  break the item; the rest lose one level), Material Return On Break (0.35), idol
  refunds on break (off), idol cost scaling (off: the game's amounts), crafting time
  (8 s + 1 s per level) and Name Seeded Rolls (off).
- Progression and idols: progress source, boss per biome, class cap, biome
idols, overrides and exclusions, idol loot removal, idol recipes and stations, and
**Blocked Items**: items that cannot be refined at the Forge (cosmetic clothing by
default). Add any item by prefab name or in-game name, for example `HelmetOdin` or
`Hood of Oden`.

## Notes

- Do not install another mod that changes the Forge of Potential at the same time.

## Updating and backups

Stop the server and close every client before updating. Back up the world's `.db` and `.fwl` files, affected character saves, and `BepInEx/config/com.sterbenden.densreforgedpotential.cfg`. Keep a copy of the previous mod version and record your dependency versions.

Replace the companion DLL on every installation together; do not leave a second copy in another plugin folder. Keep your existing configuration unless the release notes specifically instruct otherwise. Check the generated settings after an update and restart server and clients after editing them.

Existing chests retain idols already stored in them. Items already above the configured refinement limit retain their quality but cannot be refined further. A backup is the way to recover earlier item state; uninstalling does not undo refinement history.

## Multiplayer and server configuration

The mod is required on both the server and clients. With **Enable Server Sync** enabled (the default), clients receive the server's synchronized configuration. Edit the server configuration while it is stopped, then restart and reconnect clients. Editing only a client's configuration does not override synchronized server settings.

World boss progress is the default unlock source, so players in the same world share progression. **Character** progress uses each character's own boss kills instead. Installations should use matching mod and dependency versions; reconnect after updating.

## Compatibility

Use one mod to control the Forge of Potential. Other mods changing its recipes, costs, success rolls, item quality, or loot may conflict. Modded equipment can need Tier Overrides or Class Overrides when its recipes do not identify its intended biome or class. Excluded Items retain vanilla handling; Blocked Items cannot be refined at this station.

After a Valheim, BepInEx, or Jötunn update, check the release notes and try a copied world in a separate profile before updating your live server. A matching version number alone does not establish compatibility with every mod combination.

## Troubleshooting

* **The mod does not load:** verify BepInEx starts, Jötunn is installed, and there is exactly one mod DLL. Read `BepInEx/LogOutput.log` for the first load error.
* **An upgrade is blocked:** check boss progress, the selected progress source, the item class cap, and Blocked Items. At the Forge, use `drp_explain`; use `drp_catalog` to inspect the catalog.
* **The wrong idol or cost appears:** check Biome Idols, tier overrides, and cost scaling. Remove other Forge-changing mods in a separate test profile.
* **Settings differ between players:** check the server configuration, Enable Server Sync, matching mod versions, and reconnect after restarting.
* **Idols remain in a chest:** contents generated before installation are not removed. Newly generated loot follows the loot-removal setting.

When reporting a problem, include the game, mod, BepInEx and Jötunn versions; client and server mod lists; relevant settings; item prefab and quality; boss progress; steps to reproduce; and the relevant client/server logs. Remove passwords, tokens, and private server details before sharing logs.

## Uninstalling

Back up first, stop the server, and close clients. Remove the mod DLL from every installation together. Keep the configuration and backups until you have checked the world and characters. Removing the mod stops its progression, recipe, loot and roll changes; it does not restore consumed idols, broken items, or earlier item qualities. Other mods may handle above-vanilla item qualities differently.

## License

Copyright © 2026 SterbenDen. Proprietary software; see the public repository's LICENSE. Previously distributed MIT copies retain their original permissions. Valheim and dependency assets remain the property of their respective owners. This community mod is not affiliated with Iron Gate AB.
