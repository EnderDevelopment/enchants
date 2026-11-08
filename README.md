# Minecraft PvP Game Mode: Enchants

Enchants is an open-source Minecraft PvP game mode concept and design specification in which players collect character-based enchantments that function as abilities across compatible items. The mode combines enchantment collection, combat abilities, cooldowns, charges, player inventory tracking, arena protection, and a last-player-standing win condition.

## Install

1. Clone or download this repository.
2. Open `MODE_DESIGN.md` to review the complete mode rules and ability specifications.
3. Use the document as the implementation reference for a Minecraft server plugin, datapack, or compatible game-mode framework.
4. Configure the resulting implementation for a PvP arena with the required player, combat, inventory, and world-border systems.

This repository contains the mode design specification. A compatible server implementation must be created before the mode can run in Minecraft.

## Use

1. Start a round with multiple players in a protected PvP arena.
2. Enable the enchantment table.
3. Players use the roller to receive an enchantment they do not already own.
4. Players activate or benefit from their collected enchantments independently of the item they are holding, unless an ability requires a projectile or target.
5. Track enchantments, charges, cooldowns, Protection's extra-heart layer, and the enchantment table state through the inventory display and action-bar or boss-bar feedback.
6. Disable the enchantment table when rolling should be unavailable.
7. Continue combat until only one player remains.
8. Announce the last living player as the winner and disable further rolls and ability activation until the next round.

Defined abilities include offensive Blast Protection, an extra-health layer from Protection, movement through Wind Burst, charged lightning from Channeling, three-projectile Wind Charge use from Multishot, and water-triggered levitation from Frost Walker. Arena blocks remain protected by default.

---

More open source project projects by EnderDevelopment: https://github.com/EnderDevelopment

Project page: https://dash.enderdevelopment.com/community/bca4d6d1-e980-44b8-9565-7b8950fb8efd?utm_source=github&utm_medium=readme&utm_campaign=auto_publish&utm_content=bca4d6d1-e980-44b8-9565-7b8950fb8efd
