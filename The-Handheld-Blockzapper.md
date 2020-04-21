Filling Holes, Stacking walls, Replacing facades, Drawing paths, Making patterns, ...
There are plenty of uses for this rather powerful gadget. 

With its configuration and upgrades, the **Handheld Blockzapper** can place and replace blocks at a distance.
* Start by [**Left-Clicking**] a Block within range to set it as the currently selected target Material.  
The tool will try to use this selected block for placing or exchanging.
* [**Right-Click**] while **Sneaking** to open the configuration screen.  
Here you can adjust whether to place or replace blocks, an area of effect, the pattern placed, and other settings.
* Once you're finished configuring, close the screen and [**Right-Click**] at blocks within range.  
The targeted blocks will be replaced or covered by the block you chose.


## Configuration
![Configuration](https://i.imgur.com/d2Vb1Z0.png)

Hover over the different Buttons to see what they control.
* **Replace Mode** controls, whether the tool should act like a Block Exchanger, or a placement tool.  
When enabled, the surface shot at by the beam will be replaced by the selected material on the left.  
Otherwise, it will simply extend the surface outwards, placing the selected material on the surface.  
_**Note**: When replace mode is active, the tool will break and drop the previous blocks. If you upgrade the **Body** of the tool, you will be able to replace blocks with higher hardness levels._

* If **Follow Diagonals** is enabled, and the tool is able to have an area of effect,  
blocks which are only diagonally reachable will also be considered as the surface.
* If **Ignore Material Borders** is enabled, and the tool is able to have an area of effect,  
block which are of the same surface but a different material will also be considered as the effective surface.

* [**Scroll**] on the **Spread Distance** input to adjust the area of effect for this tool.  
_**Note**: Without upgraded **Amplifiers** the tool will only be able to place one block at a time._

* **Patterns** can define a certain condition under which blocks are placed.   
This is especially effective when using the tool with an upgraded area of effect.  
**Solid Material** is the default pattern and will place blocks in every position.  
**Checkerboard** only places blocks in every other space, creating a checkered surface.  
**% Roll** will randomize whether to place a block or not, there are three percentiles to choose from.


## Upgrades
There are five traits to a Handheld Blockzapper, which you can improve by upgrading it:  
(All recipes can be viewed in JEI, press 'U' hovering a blockzapper item)

---
### Area of Effect (Amplifier)
Increases the amount of blocks modified by one shot.
* Default: Max area of effect is **1x1**.
* Using **Brass**: Allows a max Area of **5x5** (3m Radius)  
* Using **Chromatic Compound**: Allows a max Area of **13x13** (7m Radius) 

---
### Speed (Accelerator)
Increases the amount of shots fired per second. Holding down [**Right-Click**] will repeat shots.  
* Default: **~2 Beams** per second
* Using **Brass**: **~3 Beams** per second
* Using **Chromatic Compound**: **~10 Beams** per second  
_Your measurements may differ due to server latencies_

---
### Range (Scope)
Increases the distance at which blocks can be manipulated.
* Default: Max range of **15m**  
* Using **Brass**: Max range of **30m**  
* Using **Chromatic Compound**: Max range of **100m**  

---
### Strength (Body)
When in **Replace Mode**, determines the maximum hardness of the blocks to be replaced.
* Default: Max allowed Hardness: 2 (Soil, Wood, Stone)
* Using **Brass**: Max allowed Hardness: 5 (Ores, Metal Blocks)
* Using **Chromatic Compound**: Anything Breakable (Obsidian, ...)  

In Creative Mode, any block can be replaced.

---
### Block Collection (Retriever)
When in **Replace Mode**, these upgrades will automatically relocate the dropped items.
* Default: Block Drops will not be relocated
* Using **Brass**: Dropped items will be relocated to the players position.
* Using **Chromatic Compound**: Dropped items will be placed in the players inventory.

In Creative Mode, replaced blocks will not drop items.
