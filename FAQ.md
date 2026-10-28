# Frequently asked questions

## Does everyone need the mod?

Yes. Install the same version on the dedicated server and every client, together with BepInExPack Valheim and Jötunn. For solo play, install it in your local game profile.

## Where do I download the installer?

Use the installer attached to the public GitHub release or the official mod-manager listing. GitHub's automatic Source code archives contain player documentation, not the installable DLL. Manual installers extract into the game/profile root under BepInEx/plugins.

## Can I install it alongside Akuichi-ReforgedPotential?

No. Remove that mod and any duplicate older copies of Den's Reforged Potential. Other mods altering the Forge, upgrade rolls, quality levels or idol recipes can also conflict.

## Do I need a new world?

The mod does not require a new world. Back up an existing world and characters before installing. Already-filled chests retain their contents, including idols; installing does not reroll them.

## Where is the Forge of Potential?

The mod uses the game's Forge of Potential in the Mountains. It does not add a replacement crafting station. Idols are crafted at their configured Workbench, Forge or Black Forge stations.

## Why can I not refine an item further?

The next band may require more boss progress, the item may have reached its class cap, or it may be blocked. Gear from a biome you have not unlocked and Deep North gear stay at their vanilla maximum. The Forge shows the next idol and current limit; use drp_explain at the Forge for details.

## Which boss unlocks the next band?

By default, defeating the previous biome's boss unlocks the next biome's band: Eikthyr for Black Forest, the Elder for Swamp, Bonemass for Mountain, Moder for Plains, Yagluth for Mistlands, the Queen for Ashlands, and Fader for Deep North. World progress is shared by default; the server can select character progress instead.

## Why do different refinements need different idols?

Every refinement belongs to a biome band and costs that band's idol. For example, a Bronze Helmet refined into the Swamp band needs Iron idols. Weapons use Battle idols; armor, shields and capes use Protection idols. Bands follow biome order rather than skipping directly to the highest unlocked idol.

## Why does light armor stop earlier than heavy armor?

Class caps keep armor and shields within the best vanilla item of the same class and slot for the unlocked biome. Light/medium, mage and heavy armor are treated separately, as are bucklers, round shields and tower shields. A higher unlocked band does not guarantee every item reaches its full band limit.

## Can a failed attempt destroy my item?

With the default Consume Idols Only On Failure enabled, a failed attempt charges the required consumables but leaves the item, quality, durability and crafter intact. Upgrade Chance defaults to 50 percent. If the server disables that option, Break Chance controls the share of failures that destroy the item; other failures lose a level. Read the server settings before attempting valuable upgrades.

## Why does reloading not change an upgrade result?

Rolls remain fixed per character, item and level. By default the character's random ID replaces name-based seeding, so choosing a different character name cannot select a favorable outcome. Name Seeded Rolls restores the game's name-based behavior when enabled.

## Where did idol drops go?

Remove Idols From Loot is enabled by default. It removes idols from newly rolled loot and trader stock; craft them from biome materials instead. Chests populated before installation keep their existing items. Recipe ingredients and stations are configurable.

## Where do I change the settings?

Start once, then edit BepInEx/config/com.sterbenden.densreforgedpotential.cfg while the server/game is stopped. Enable Server Sync defaults to on, so multiplayer clients use the synchronized server settings. Restart and reconnect after changes.

## What is the difference between blocked and excluded items?

Blocked Items cannot be refined at the Forge at all; cosmetic clothing is blocked by default. Excluded Items are left to vanilla handling. Tier and Class Overrides are available for equipment that needs a different classification.

## Can I keep items already above the limit?

Yes. They keep their current quality but cannot be refined further while above the applicable limit. Changing settings or removing the mod does not automatically restore a previous quality or refund materials.

## How should I update or uninstall safely?

Stop the server and clients, back up worlds, characters and configuration, and update or remove the DLL everywhere together. Preserve the old version for recovery and avoid duplicate DLLs. Use a separate profile and copied saves to test compatibility after game updates. Uninstalling does not undo earlier refinements or recover broken items.

## What should I include in a bug report?

Report through the public GitHub issues page. Include game and mod/dependency versions, client/server mod lists, relevant configuration, item name or prefab and quality, progress state, reproduction steps and BepInEx logs. Remove credentials and private server details before posting.
