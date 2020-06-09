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

Run `/reload` and you should see this recipe in JEI (if you have installed JEI), or just try it.

![Imgur](https://i.imgur.com/ZoGDVdx.png)

*Note: In Create 0.2.3 the id is crushed_zinc, in Create 0.2.4+ it is crushed_zinc_ore!*

Adding crafting recipes is just as easy, [this tool](https://crafting.thedestruc7i0n.ca/) might be helpful.

## Removing recipes (CraftTweaker needed)

To remove a recipe, run `/ct dump recipes`. This command will dump all active recipes in the *crafttweaker.log* file in the logs folder. There you can check the path a recipe has.

To remove the recipe, make a new *.zs* file in the scripts folder of your Minecraft (only there if CT is installed), and add a line like `<recipetype:create:splashing>.removeByName("create:splashing/soul_sand");`

This line would remove the soulsand splashing recipe. To remove other recipes, you have to change the recipe type and the recipe name.

## Tags

To use a tag in crafting recipes, use `"tag": "modname:tag_name"`

For example, `"tag": "forge:ingots/copper"`would accept all copper ingots that are added to the ingots/copper tag.

Tags can only be used as ingredients.

