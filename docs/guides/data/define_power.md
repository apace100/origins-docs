---
title: Defining a Power
date: 2021-05-02
---
# Defining a Power in JSON

Powers are used by Origins to define functionality. Each Origin is a set of these powers. Since Origins v0.4.0, powers are data-driven, allowing you to change and add powers via datapacks.

In order for the game to load powers, they have to go in the correct path of the data pack. The full path of a power file should look like this: `data/<namespace>/powers/<power_id>.json`.

Generally, all powers support the fields found on this page: [Power JSON](../../power_json.md). For all other fields which define more specific functionality of a power, you will have to look at the page corresponding to the power type you want to use. A list of power types can be found here: [Power Types](../../power_types.md)

### Tutorial

**Important:** this example guides you through creating a custom power. It is required for you to have read and understood [Defining an Origin](define_origin.md) first!

Say we want to create a power which burns undead entities when an origin with this power hits them. Let's call this power "Holy Fire". To start, let's create a file in `data/<namespace>/powers/holy_fire.json`. It's always a good idea to select file names which match the names of the power you are creating. Don't forget that the `<namespace>` part needs to be exchanged with the namespace of your datapack (basically an ID which specifies your datapack). Since this is a tutorial, I'm going to name it `tutorial`, and therefore the full path for me would be `data/tutorial/powers/holy_fire.json`. Due to the power being located at this path, it has the ID `tutorial:holy_fire`. This will be important later on.

Most often, if you want to do something to a target you're hitting, the [Target Action On Hit](../../power_types/target_action_on_hit.md) will be the power type you are looking for. That means we should start the content of our power file like this:

```json
{
	"type": "origins:target_action_on_hit",
	"name": "Holy Fire",
	"description": "Your divine grace sets the undead ablaze when you hit them."
}
```

I took the liberty of directly adding a `name` and `description` field. This will be the name and description of the power that show up when a player views your origin.

Now, onto the actual functionality. As can be seen on the [Target Action On Hit page](../../power_types/target_action_on_hit.md), there are two fields which are required: a `cooldown` and an `entity_action`. The cooldown is just a number which describes the time this power needs to recharge after it was executed. Since we want our power to apply on every hit, let's set it to 1, which means the cooldown is 1/20th of a second (it can't be any less than 1, and you wouldn't even be able to hit twice in 1 "tick"). The `entity_action` is more complex, and defines what exactly should happen to the entity we're hitting.

```json
{
	"type": "origins:target_action_on_hit",
	"name": "Holy Fire",
	"description": "Your divine grace sets the undead ablaze when you hit them.",
	"cooldown": 1,
	"entity_action": {

	}
}
```

As you can see from the JSON above, I already began adding the `entity_action` field, by starting with another set of curly braces (`{}`). This is because an `entity_action` is an [object](../../data_types/object.md), which requires a `type` field, which then defines the further parameters it supports. Essentially, this is similar to what we're already doing with the power (specifying a type and then defining all it needs), just this time it's about an [entity action](../../entity_actions.md)! Having a look at the list, the [Set On Fire action](../../entity_actions/set_on_fire.md) looks exactly like what we want, and it just requires a single `duration` field which specifies the amount of seconds the entity should burn. I decided to go with 4 seconds:

```json
{
	"type": "origins:target_action_on_hit",
	"name": "Holy Fire",
	"description": "Your divine grace sets the undead ablaze when you hit them.",
	"cooldown": 1,
	"entity_action": {
		"type": "origins:set_on_fire",
		"duration": 4
	}
}
```

Now that everything that was listed as required has been defined, this power should actually run! Go ahead and add the namespaced ID we talked about before (depends on the path to your power file), in my case `tutorial:holy_fire`, to your origin's power list, and you should be able to see it in-game and test it out.

Doing that, you probably noticed that this power burns everything you hit, not just undead mobs! Makes sense, because there is nothing in our power file which says it should only apply to undead mobs. To fix this, we'll make use of the optional field `target_condition` listed on the [Target Action On Hit page](../../power_types/target_action_on_hit.md), which allows us to specify exactly which targets we want to apply our effect to. This field requires an [entity condition](../../entity_conditions.md), meaning it is an [object](../../data_types/object.md) just like the `entity_action` we specified earlier. Looking through the conditions, the [Entity Group condition](../../entity_conditions/entity_group.md) allows us to check for a mob being undead, so let's use that! It works by specifying the entity group we want as a string, which in our case would be `undead`:

```json
{
	"type": "origins:target_action_on_hit",
	"name": "Holy Fire",
	"description": "Your divine grace sets the undead ablaze when you hit them.",
	"cooldown": 1,
	"entity_action": {
		"type": "origins:set_on_fire",
		"duration": 4
	},
	"target_condition": {
		"type": "origins:entity_group",
		"group": "undead"
	}
}
```

With the target condition in place, this power now does exactly what you want: when a player with this power hits an undead mob, the mob begins to burn for 4 seconds!

Hopefully this tutorial has shed some light into the process of creating powers, and allows you to bring your own ideas to life. I encourage you to browse through the different pages for actions, conditions and power types, to get a feeling for what's possible and what isn't. Having a rough idea of what exists also helps immensely with knowing how to turn a power concept you might have into reality.

### Related pages

* [Power Types](../../power_types.md)
* [Power JSON](../../power_json.md)
* [Origin JSON](../../origin_json.md)
