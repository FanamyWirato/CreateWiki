Belt observers are a redstone based component capable of detecting and ejecting items on [[Mechanical Belts|Mechanical Belt]]

## Crafting

Requires 1 Redstone Dust, 1 Observer, 1 Iron Ingot, and 1 [[Brass Casing]].

![](https://i.imgur.com/aRaEZXO.png)

## Usage

Belt observers must be placed next to a non-angled belt. Belt observers are incompatible with belt sections that have embedded shafts, but are compatible with belt sections reinforced with [[Brass Casing]].

![](https://i.imgur.com/kexBJ58.png)

Belt observers have a filter slot, able to accept items, [[Item Filters, and Attribute Filters|Filter]].

Belt observers have four operating modes. Modes can be cycled with the [[Wrench]].

![](https://i.imgur.com/rfDLSNP.png)

## Detect mode

Outputs a redstone signal if an item matching the filter slot is present anywhere on the adjacent belt section. This signal is continuous, and will last for as long as the item is on the belt.

## Pulse mode

Outputs a short redstone pulse when an item matching the filter slot passes through the center of the adjacent belt section. Unlike detect mode, this signal is not continuous, even if the belt is paused with the item still in the center of the belt.

## Eject mode

Identical to pulse mode, except that items matching the filter slot will be instantly pushed off of the belt, away from the Belt Observer. This will either place the item as an entity in the world, or if another belt is one block away, onto that belt. If an entity or an item is blocking the way, the item on the belt will stall and the Belt Observer will emit a continuous signal until the blockage is cleared.

## Split mode

Identical to eject mode, except that only half of the items in a stack are ejected. If the stack is odd and cannot be split evenly, the extra item is kept and not ejected.

## Mob detection

All modes of the belt observer emit a continuous redstone signal if a mob is on the relevant belt section while the belt is moving. There is no way to blacklist mobs from detection. Mobs are not affected by the eject or split modes.