# 1.0.4
* Upgrade Settings are back: Upgrade Chance, Break Chance, Consume Idols Only On
  Failure, Material Return On Break, idol refunds on break, idol cost scaling and
  crafting time.
* New defaults: 50% Upgrade Chance, and a failed upgrade only uses up the idols and
  materials; the item itself is left untouched (same level, durability and crafter)
  and never breaks. Turn off Consume Idols Only
  On Failure for the game's behaviour (Break Chance 1 = the item breaks).
* Forge rolls are seeded from the character's random ID instead of its name, so a
  name can no longer be picked to win an upgrade. Name Seeded Rolls restores the
  game's behaviour.

# 1.0.3
* New Blocked Items setting: items that cannot be refined at the Forge of Potential.
  Blocks the cosmetic hats, dresses, tunics and Harvester outfits by default and
  accepts prefab names or in-game names, so newly added cosmetics can be listed too.

# 1.0.2
* Fix: the Forge line (next idol, limit and progress) was erased by the game every
  frame and never shown; it now stays under the item description.
* Fix: idols could still drop from chests and traders placed by locations and dungeons.
  Idols are now removed wherever loot is rolled (chests, pickables, creature drops,
  trader stock). Chests generated before installing keep their contents.

# 1.0.1
* New package icon taken from the game.

# 1.0.0
* Biome progression for the Forge of Potential with the vanilla Forge unchanged.
* Refinement levels in biome bands following vanilla's per-level steps, unlocked by
  world (or character) boss progress.
* Each refinement costs the idol of its band's biome; no biome is skipped.
* Class cap keeps light, heavy and mage armor and each shield type in their lines.
* Item biome from crafting materials and station.
* Idols are craftable from biome materials and removed from all loot.
* `drp_catalog` and `drp_explain` console commands.
