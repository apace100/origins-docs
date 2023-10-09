---
title: Defining an Origin
date: 2021-05-02
---

# Defining an Origin in JSON

Origins are defined in JSON files. Let's use these to create a fictional new origin, a _Supermorph_, for our [Data Pack](https://minecraft.wiki/w/Data_Pack) which we call _OriginSuperPack_. We'd like this Origin to be a bit overpowered: Metamorphs are immune to fire, have Elytra Flight and can teleport with ender pearls. Their only drawback is that they need a bed at a high altitude, just like Avians. This would be a JSON file which would accomplish that:

```json
{
	"powers": [
		"origins:fire_immunity",
		"origins:elytra",
		"origins:throw_ender_pearl",
		"origins:fresh_air"
	],
	"icon": "minecraft:slime_ball",
	"order": 4,
	"impact": 1
}
```

This is the JSON file defining our new _Supermorph_ origin. We put it in `data/originsuperpack/origins/supermorph.json`. In general, the file location should be as follows: `data/<namespace>/origins/<path>.json`. You can also use the namespace `origins` and the name of an existing origin, such as `avian`, in order to override the origin defined by the default mod: `data/origins/origins/avian.json`. **But do remember to add a `loading_priority` field to the file that is higher than the original origin's** (for all origins that come with the base mod, that value is `0`).

When you put the file in the correct file structure of a data pack and put it into a world (either when you create the world, or after the world is loaded drag it into the world's `datapacks` folder), the new origin still does not appear! Why? **Layers.**

The new origin still needs to be added to the origin layer. Layers are the way that Origins has to allow players to have multiple origins. By default, there is only one layer, `origins:origin`. If you wanted, you could create your own layer and allow players to select a second origin! Here's how to add our origin to the default origin layer though: we need to create a layer file with the same ID of the layer we want to add to. This means our file should be located in `data/origins/origin_layers/origin.json`. The file content would then look like this:

```json
{
	"replace": false,
	"origins": [
		"originsuperpack:supermorph"
	]
}
```

`replace` just tells Origins that we want to add to the already existing layer, instead of replacing it entirely. The `origins` field meanwhile specifies the IDs of the origins we want to append to the layer. See below for a complete description of the layer format (which is relevant if you want to create your own layer).

Now, our newly created _Supermorph_ origin should show up, along with a nice slimeball icon, in the list.

However, the origin still doesn't display a correct name or description. One way to fix that is by adding a [Resource Pack](https://minecraft.wiki/w/Resource_Pack) as well, with a translation for the language you're playing in (probably `en_us.json`):
```json
{
	"origin.originsuperpack.supermorph.name": "Supermorph",
	"origin.originsuperpack.supermorph.description": "The Supermorphs are crazy origins which I created for a tutorial!"
}
```

Instead of adding these to a resource pack though, which would be required on the client-side, Origins also allows setting a name and description in the datapack. To do that, just add a `name` and a `description` field to the JSON file defining your origin, like this:

```json
{
	"powers": [
		"origins:fire_immunity",
		"origins:elytra",
		"origins:throw_ender_pearl",
		"origins:fresh_air"
	],
	"icon": "minecraft:slime_ball",
	"order": 4,
	"impact": 1,
	"name": "Supermorph",
	"description": "The Supermorphs are crazy origins which I created for a tutorial!"
}
```

That concludes this tutorial on how to define custom origins using existing powers. If everything works, the next step would be to learn how to [add a custom power](define_power.md)

### Related pages

* [Origin JSON](../../json/origin.md)
* [Upgrade JSON](../../json/upgrade.md)
* [Layer JSON](../../json/origin_layer.md)
