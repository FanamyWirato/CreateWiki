_Punches_, _Uses_, and _Activates_. This machine will try to _imitate_ a _player_ as a best as it can. _Takes_ and _Deposits_ _items_ into an adjacent _Inventory_. Can be assigned an item-stack as a _filter_.

![](https://i.imgur.com/DHKEtuO.jpg)

The Deployer is a component that is extremely versatile in use. It can simulate several interactions that would otherwise be done manually. In order to run, it needs constant rotational force, and its speed correlates to the rotational speed of the input.  

## Setting up

* Deployers activate in the block space that is **2m in front of them**. Between the active area and the deployer can be any other block, it will be ignored/phased through.
* When the Deployer is supposed to use items, they can either be handed to it via right-click, or from an inventory anywhere adjacent to the component. To ensure that Deployers pull items from inventories, apply a [[filter to its filter slot|Filtering]], matching only the desired items. 
* Using a **Wrench** on the front face of a Deployer toggles the mode between **Use** and **Attack**. This corresponds to whether a player would click with the right or the left mouse button.
* When a Deployer **obtains items** from activating something, it will dispose of them once retracted. If there is no inventory adjacent to it, the items will simply be ejected at the back.

![](https://i.imgur.com/tHfYdsn.jpg)

This Deployer is set up to only activate when an **Empty Bucket** is held (filter slot). Since there is a chest next to it and it has a filter, it will wait until it's able to pull one from the inventory. Once activated, the filled buckets will be dropped back into the chest.

<br><br><br>

## Usage Scenarios

![](https://i.imgur.com/1r2QH2S.jpg)
**Block activation**: Use mode; no held items. Examples:
* Opening doors
* Pushing buttons
* Pulling a [[Hand Crank]]
* Clearing a [[Basin]]
<br>

![](https://i.imgur.com/V3l6UZZ.jpg)
**Using items on Blocks**: Use Mode with held item. Examples:
* Igniting TNT (image)
* Stripping logs
* Fertilizing Saplings
* Picking up or Placing Fluids
<br>

![](https://i.imgur.com/IUcm1DD.png)
**Using items**: Use Mode with held item, no block in active area. Examples:
* Automated [[Sandpaper]] polishing (image)
* Milking Cows
* Shearing Sheep
* Throwing Snowballs or Eggs
* Eating Consumables (Has no purpose)
<br>

![](https://i.imgur.com/Y4ofR9C.jpg)
**Placing Blocks**: Use Mode with held block, no block in active area.
* Simulates placing a block with the held item
<br>

![](https://i.imgur.com/DytyxmG.jpg)
**Punching Blocks**: Attack Mode; no held items. Example:
* Activating Note Blocks (image)
<br>

![](https://i.imgur.com/S9k0YXl.jpg)
**Attacking Entities**: Attack Mode; no block in active area.
* Drops player-specific entity drops
* Killed entities do not spawn experience orbs
<br>

![](https://i.imgur.com/gVbi9Gm.jpg)
**Breaking Blocks with Item**: Attack Mode with held item; block in active area.
* Simulates breaking the block with the held item.

<br><br>

## Item Display
![](https://i.imgur.com/gnkxwUi.jpg)  
Vertical Deployers in Use mode will present their held items in a more aesthetic fashion.  
Once rotation is supplied, they will still activate normally.

<br><br>

## Portability
![](https://i.imgur.com/Y9aabgZ.jpg)
* Deployers can be mounted on [[Moving Contraptions]]. They will activate just like they would when stationary, once for every block position they visit.
* Deployers hold on to their items and filter when moved, however they will not be rendered.
* If [[Portable Inventories]] are mounted on the same structure, the moving Deployer will use those similarly to the adjacent inventories in stationary Mode. On the structure they do not have to be adjacent.