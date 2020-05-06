The **Funnel** is an advanced mechanical component that functions alongside the [[Extractor]] and the [[Transposer]] as part of Create's system of moving items in and out of inventories. The Funnel is used for taking items from the world and from [Mechanical Belts](Mechanical-Belt) and placing them in advanced inventories.

## Usage

### Passive item intake
A funnel can be placed on any side of any block that has an inventory, such as an [[Adjustable Crate]]. Any item that ends up in the block space containing the funnel will automatically be placed in the attached inventory.

If a [[Mechanical Belt]] is in the block directly below the funnel, items on the belt will be taken by the funnel, and the funnel's sprite will change to reflect that. If the attached inventory becomes full, the funnel will cause items on the belt to stall.

### Filtered item intake
The funnel has a filter slot in which any item can be placed, thereby setting the funnel to only take in the specified item. Alternatively, a [[Filter]] or [Attribute Filter](Filter) can be placed in the slot to have more precise control over what items are and are not taken by the funnel. This can be used as a component for [bulk item processing](Encased-Fan) such that items will not be taken by the funnel until the relevant processing recipes have been applied.