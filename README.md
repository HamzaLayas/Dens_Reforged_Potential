# Den's Reforged Potential

Biome progression for the Forge of Potential. The mod decides how far each item can
be refined and which idol each refinement costs, and makes the Forge's odds
configurable. By default an upgrade succeeds half of the time, and a failed upgrade
only uses up the idols: the item keeps its level and never breaks.

**Required on the server and on every client.**

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
