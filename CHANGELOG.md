# Changelog

## 1.0.5

Documentation update. Gameplay behavior is unchanged. Install the same mod version on the server and every client.

* Expanded the player guide with installation, configuration, multiplayer, backup, update, compatibility and troubleshooting help.
* Added a 17-question FAQ covering refinement limits, boss progress, idols, failed upgrades, server settings and existing saves. The FAQ is included on the public player page and in the Hexium package.
* Download and support links now point to Den's Reforged Potential's public GitHub page.

## 1.0.4

Upgrade settings return, with safer defaults for failed attempts. Check the server's settings before refining valuable equipment.

* New default: upgrades have a 50% success chance. A failed attempt consumes the required idols and materials but preserves the item's quality, durability and crafter.
* Added settings for success chance, item break chance, material returns, idol refunds, increasing idol costs and crafting time.
* **Consume Idols Only On Failure** is enabled by default. If disabled, failures can destroy the item or reduce its quality according to **Break Chance**. A Break Chance of 1 makes every failed attempt destroy the item.
* Choosing a character name no longer lets players select favorable upgrade results. Outcomes remain fixed for each character, item and level, so reloading does not change a result. **Name Seeded Rolls** restores the game's name-based behavior when enabled.

## 1.0.3

* Added **Blocked Items** so server owners can prevent selected equipment from being refined at the Forge of Potential.
* Cosmetic hats, dresses, tunics and Harvester outfits are blocked by default. Additional items can be listed by prefab name or in-game name.

## 1.0.2

* Fixed the Forge's next-idol, refinement-limit and progress information disappearing from the item description. It now remains visible while viewing the item.
* Fixed idols still appearing in some location and dungeon chests and trader inventories. Idol removal now covers newly generated loot and trader stock. Chests filled before installing retain their existing contents.

## 1.0.1

* Updated the mod's package icon using artwork from Valheim.

## 1.0.0

Initial release. Required on the server and every client.

* Added biome-based refinement progression at the existing Forge of Potential. Additional levels unlock as bosses are defeated, using shared world progress by default or each character's progress when configured.
* Refinements advance through biome bands and use that band's idol, keeping idol costs in biome order.
* Added armor and shield limits that keep equipment within its class: light, heavy and mage armor remain distinct, as do the different shield types.
* Equipment is assigned to a biome using its crafting materials and station, with configurable overrides for items that need a different classification.
* Added craftable idols made from biome materials and removed idols from newly generated loot.
* Added **drp_explain** to explain the selected Forge item's requirements and **drp_catalog** to list equipment and its refinement limits.
