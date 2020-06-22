Create uses the JSON recipe format introduced first in Minecraft 1.13. You can change Creates recipes by using your own data pack to fit your needs. Whether you are a pack-maker or a casual player just wanting to add new options, this article will guide you through the basics of data packs, openloader (a mod by Darkhax) and CraftTweaker (a mod by Jared) to cover all your needs of changing recipes.

## What is a data pack?

As of the [Minecraft Wiki](https://minecraft.gamepedia.com/Data_Pack), "the data pack system provides a way for players to further customize their Minecraft experience". A data pack can contain code in the form of command block contraptions without command blocks, **extra recipes**, custom loot tables (mob and block drops, chest loot), new advancements, **tags** (can be used in recipes for groups of items), and dimensions. As this guide will help you with custom recipes, we will look mainly at recipes and tags. As of vanilla, data packs are added to a world. You can do this, but if you want to ship global recipes with your pack without shipping a world, openloader is a great tool for that.

## What do I need?

**Editor:** At minimum, you need access to your Minecraft folder and a text editor. But writing JSON in a simple text editor with no highlighting is no fun. Therefore, a text editor with JSON highlighting and syntax validation is *very* useful. You can use Notepad++ with an addon, Eclipse with addon, any idea IDE, the options are endless.

**[Openloader](https://www.curseforge.com/minecraft/mc-mods/open-loader) (optional):** Openloader by Darkhax is a utility mod that gives a modpack author the option to add global data packs. It is a mod available for 1.14.4 and 1.15.2 and does not demand any performance.

**[CraftTweaker](https://www.curseforge.com/minecraft/mc-mods/crafttweaker) (optional):** CraftTweaker can help you get all currently active recipes and see the tags an item is part of. This makes CraftTweaker an excellent mod to debug your recipes in-game. But, most importantly, CraftTweaker allows for a clean removal of recipes. If you add a new recipe, you will often want the old recipe gone. If this recipe is added by the mod natively (in the .JAR), CraftTweaker is the best option to disable it.

**[JEI](https://www.curseforge.com/minecraft/mc-mods/jei) (optional):** To see your changes quickly, Just Enough Items is recommended. You can get along without it, but it is a very useful tool and will be used in this article as tool to show the effect of changes.

***Note: None of these mods is developed by the Create developer team, the Create developer team is not responsible for any problems you might have with these mods!***

### The Setup

To start data pack developing, you need to place your root folder of the data pack in either the save folder */saves/world_name/datapacks*/***your_data_pack_root_dir*** or the openloader folder */openloader/data/**your_data_pack_root_dir***. It is advisable to call that data pack root directory in a way you want it to show up in game with the command `/datapack list`. **The name may not start with a number and may only contain lower case letters, numbers and underscores!!!**

In that data pack root folder, you need a file called *pack.mcmeta* which contains data pack information. A sample of a *pack.mcmeta* file would be

```json
{
	"pack": {
		"pack_format": 5,
		"description": "Your interesting description"
	}
}
```

Apart from *pack.mcmeta*, you need a *data* on the same layer. Inside, there has to be a new folder called ***your_data_pack_name*** (of course your name goes here, not this exact text).

 Inside, you can place two folders, *recipes* and *tags*.

![File Structure of a Minecraft data pack](https://i.imgur.com/nfsj3lx.png)

With these steps complete, restart your game or run the command `/reload` to load your changes (`/relaod` is faster), and do `/datapack list` to see whether your data pack shows up.

![Imgur](https://i.imgur.com/ttt9Epo.png)

If the data pack does not show up, check the file structure. If it shows up in red as available, run 

`/datapack enable "file/your_data_pack_name"` to enable the data pack and rerun the list command to check.

A full setup with these steps can be found [here](https://github.com/LordGrimmauld/data_pack).

## Adding a recipe

Recipes are written in JSON. Examples of recipes can be found in the [Create Github](https://github.com/Creators-of-Create/Create/tree/master/src/main/resources/data/create/recipes), these might help as orientation.

To start, add a new JSON file to the recipe folder (same naming conventions as for the data pack name, file extension is *.json*) in which the recipe will be added. There has to be one JSON file per added recipe.

This first example recipe will make crushed zinc obtainable by washing lime sand.

F3 + H gives you information on item IDs which you need to specify which items should be used for the recipe.

```json
{
    "type": "create:splashing",
    "ingredients": [
    	{
    		"item": "create:limesand"
    	}
    ], 
	"results": [
		{
			"item": "create:crushed_zinc_ore",
			"count": 1,
			"chance": 0.1
		}
	]
}
```
*Note: chance is optional and 1.0 by default*

Run `/reload` and you should see this recipe in JEI (if you have installed JEI), or just try it.

![Imgur](https://i.imgur.com/ZoGDVdx.png)

*Note: In Create 0.2.3 the id is crushed_zinc, in Create 0.2.4+ it is crushed_zinc_ore!*

Adding crafting recipes is just as easy, [this tool](https://crafting.thedestruc7i0n.ca/) might be helpful.

## Removing recipes (CraftTweaker needed)

To remove a recipe, run `/ct dump recipes`. This command will dump all active recipes in the *crafttweaker.log* file in the logs folder. There you can check the path a recipe has.

To remove the recipe, make a new *.zs* file in the scripts folder of your Minecraft (only there if CT is installed), and add a line like `<recipetype:create:splashing>.removeByName("create:splashing/soul_sand");`

This line would remove the soulsand splashing recipe. To remove other recipes, you have to change the recipe type and the recipe name.

## Tags
In the way of creating/modifying recipes you can write `tag` instead of `item` in the ingredients section, therefore you need to use the tag of an item and not the ID.

You can view the tags and ID of an item when using JEI and pressing shift (default) while hovering over the item.

### What is a tag
In addition to the ID items can have a tag too, while the ID (identifier) must be unique, tags can be used on multiple items. You could also call it grouping or relate to hashtags.

So each item has one unique ID, but can has from none to many tags.

![Imgur](https://imgur.com/i6V8oSg.png)
![Imgur](https://imgur.com/O8eUY5v.png)
![Imgur](https://imgur.com/TcFxfXe.png)
![Imgur](https://imgur.com/8T9cdaH.png)

*These examples shows you that every item has a unique ID and the same tag.*

### Using tags
#### Tags in the ingredients section
If you want to create a recipe which should accept every crushed_ore, you don't need to write a recipe for every crushed_ore. One is enough and it should look like this:
```
{
    "type": "create:milling",
    "ingredients": [
        {
                "tag": "create:crushed_ores"
        }
    ], 
        "results": [
                {
                        "item": "my_mod:my_example_pulver",
                        "count": 1,
                }
        ]
}
```
*Note: the result must always include the item and don't forget to change the item of the result*

Another example - taken from the press recipe for brass ingots.
```
{
    "type": "create:pressing",
    "ingredients": [
    	{
    		"tag": "forge:ingots/brass"
    	}
    ], 
	"results": [
		{
			"item": "create:brass_sheet",
			"count": 1
		}
	]
}
```

#### Tags in the results section
Tags can be added in the result section to achieve further functionality for items.
If you're interesed in this topic you can read [further](https://minecraft.gamepedia.com/Tag).

## List types added/advanced by Create
| Machine                             | Type                                            | Shaped Crafting | Multiple Ingredients | Additional Parameter                                                                                                 |
|-------------------------------------|-------------------------------------------------|-----------------|----------------------|----------------------------------------------------------------------------------------------------------------------|
| Millstone                           | create:milling                                  | No              | No                   | processingTime\<ticks\>                                                                                                |
| Crushing Wheel                      | create:crushing                                 | No              | No                   | processingTime\<ticks\>                                                                                                |
| Mechanical Press                    | create:pressing                                 | No              | No                   |                                                                                                                      |
| Mechnical Mixer                     | create:mixing                                   | No              | Yes                  | For ingredients: return_chance \<double\>, 1.0 = 100% `{"item": "minecraft:blaze_rod", "return_chance": 0.97 }` |
| Mechinal Press + Basin (Compacting) | crafting_shaped, crafting_shapeless | Yes             | No                   | The Compacting looks for squared shaped recipes with the same items                                                     |
| Mechanical Sawing                   | create:cutting                                  | No              | No                   | processing_time\<ticks\>                                                                                                      |
| Mechanical Cutting                  | minecraft:stonecutting                          | No              | No                   |                                                                                                                      |
| Encased Fan + Water                 | create:splashing                                | No              | No                   |                                                                                                                      |
| Encased Fan + Lava                  | minecraft:smelting                              | No              | No                   | cookingtime\<ticks\>, experience\<double\>                                                                               |
| Encased Fan + Fire/Campfire         | minecraft:smoking                               | No              | No                   | cookingtime\<ticks\>, experience\<double\>                                                                               |
| Sandpaper Polishing                 | create:sandpaper_polishing                      | No              | No                   |                                                                                                                      |
| Mechanical Crafter                  | create:mechanical_crafting                      | Yes             | Yes                  | Shaped Crafting is needed                                                          |
### Compacting Shapes
As the compacter searches for crafting_shaped and crafting_shapeless recipes some extra needs need to be fullfilled.
1. the structure must be in a square shape (without spaces in the pattern)
```
AA
AA
```
```
AAA
AAA
AAA
```
2. Only 1 key(item) is allowed for the pattern.

### Mechincal Crafter
The crafter takes different Shapes, it could take up to 100 blocks for width and height (untested)

It was safely tested for up to 9x9 (including JEI), with 10 or more, JEI isn't able to show it anymore.

Example: the recipe in version 0.2.4 for the crushing wheel
```
"pattern": [
			" PPP ",
			"PSBSP",
			"PBCBP",
			"PSBSP",
			" PPP "
        ],
        "key": {
			"P": {
                "item": "create:andesite_alloy"
            },
            "S": {
                "tag": "forge:rods/wooden"
            },
			"C": {
                "item": "create:andesite_casing"
            },
			"B": {
                "tag": "forge:stone"
            }
        },
```

## Useful links
For some more examples or help on types, just check the data-pack recipes create already includes.
[Click me](https://github.com/Creators-of-Create/Create/tree/mc1.15/dev/src/main/resources/data/create/recipes)