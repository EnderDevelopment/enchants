# I Become a Mace

## Mode Summary

Players collect enchantments that attach to their character instead of to individual items. A collected enchantment works while the player uses any compatible item, and the player can see every collected enchantment in their inventory screen.

The enchantment table is a mode object that can be turned off. When it is off, players cannot roll or receive new enchantments from it.

## Core Rules

- Enchantments are stored per player.
- Normal item enchantment restrictions do not apply to collected enchantments.
- A collected enchantment affects the player regardless of which item is held.
- Duplicate enchantments do not stack unless an effect explicitly defines levels.
- The inventory display lists every collected enchantment and its current charge or cooldown.
- The enchantment table has an enabled or disabled state.
- The mode should announce major ability activations to the affected player and show cooldowns without filling chat.

## Enchantment Roller

The roller gives a player one available enchantment from the mode's enchantment pool. A roll must not award an enchantment that the player already owns. If the player owns every enchantment, the roller gives no duplicate reward and reports that the collection is complete.

Rolling is blocked while the enchantment table is disabled. The table's state must be visible to players through its block state, interaction message, and inventory display.

## Confirmed Custom Effects

### Blast Protection

Blast Protection becomes an offensive ability rather than ordinary armor protection.

- The player can trigger a controlled explosion at the targeted point within the ability range.
- The explosion damages nearby enemies and applies knockback.
- The ability must not damage the activating player unless the mode explicitly enables self-damage.
- Blocks should remain protected by default so the ability does not destroy the arena.
- A cooldown prevents repeated activation.

### Protection

Protection creates an additional layer of player health.

- The player receives one extra layer of hearts while Protection is owned.
- The extra layer is consumed before the player's normal health.
- The layer regenerates only through the mode's defined regeneration rule; ordinary healing must not duplicate it.
- Losing Protection immediately removes the extra layer and clamps health to the valid maximum.

### Wind Burst

Wind Burst is a universal movement ability.

- It can be activated while holding any item.
- Activation launches the player upward and forward using a mace-like wind burst.
- The ability uses a cooldown and cannot be triggered while its cooldown is active.
- The effect applies to the activating player and does not require a normally enchanted mace.

### Channeling

Channeling charges through successful melee hits.

- Every valid melee hit adds one charge.
- Ten valid hits fully charge the ability.
- A fully charged hit calls down lightning on the struck target.
- The lightning effect works with any held item.
- Misses, environmental damage, projectile damage, and self-damage do not add charge.
- After lightning is released, the charge returns to zero.

### Multishot

Multishot modifies projectile use for every compatible projectile action.

- When the player uses a wind charge, the ability releases three wind charges in a spread.
- The spread has a center projectile and two angled projectiles.
- The ability does not require a crossbow.
- Each activation consumes the normal resource once, not three times.
- The effect has a short cooldown to prevent projectile spam.

### Frost Walker

Frost Walker changes from freezing water into a levitation ability.

- When the player touches or moves over water, the player levitates above the water surface.
- No temporary ice blocks are created under the player's feet.
- The effect ends when the player leaves the water area or when the ability duration expires.
- The ability must not allow uncontrolled vertical flight or bypass the mode's world border.

## Universal Enchantment Behavior

Every enchantment in the mode is treated as a character ability. The original Minecraft item effect is replaced or adapted by the mode effect. An enchantment may be passive, triggered, charged, or cooldown-based, but it must always be usable independently of the item held unless its specific effect requires a projectile or target.

A player can have multiple enchantments active at the same time. Effects must be resolved independently so one ability cannot silently remove another ability's charge, cooldown, or health layer.

## Inventory Display

The player inventory must show:

- Every collected enchantment.
- Whether each enchantment is passive, ready, charging, or on cooldown.
- Channeling's current hit count out of ten.
- Protection's current extra-heart layer.
- The enchantment table's enabled or disabled state.

The display should update immediately after a roll, hit, ability activation, cooldown change, or enchantment removal.

## Player Feedback

Use action-bar or boss-bar feedback for temporary state:

- Ability ready.
- Ability activated.
- Ability on cooldown.
- Channeling charge progress.
- Enchantment table disabled.
- Collection complete.

Keep combat feedback out of normal chat unless an event affects every player.

## Arena Safety

The mode should protect the arena from permanent terrain damage. Blast Protection explosions and Channeling lightning may create visual and sound effects, but the arena should be restored or block damage should be disabled. Player damage, knockback, fire, and status effects remain enabled according to the server's normal combat rules.

## Win Condition

The default win condition is the last living player. When one player remains, the mode ends, announces the winner, and disables further enchantment rolls and ability activation until the next round.
