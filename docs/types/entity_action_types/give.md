---
title: Give (Entity Action Type)
date: 2021-04-06
---

# Give

[Entity Action Type](../entity_action_types.md)

Gives the entity an item stack by inserting it into its inventory or dropping it on the ground if there is no available inventory space.

Type ID: `apoli:give`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`stack` | [Item Stack](../data_types/item_stack.md) |  | The item stack to give to the entity.
`item_action` | [Item Action Type](../item_action_types.md) | _optional_ | If specified, the specified item action type will be executed on the item stack before it's given to the player.
`preferred_slot` | [String](../data_types/string.md) | _optional_ | If specified, this will prioritize the action to put the item in the specified slot. Accepts `"chest"`, `"feet"`, `"head"`, `"legs"`, `"mainhand"` or `"offhand"`.


### Examples

```json
"entity_action": {
  	"type": "apoli:give",
  	"stack": {
	  "item": "minecraft:egg",
	  "amount": 3
  	}
}
```

This example gives the entity 3 Eggs.
<br>

```json
"entity_action": {
	"type": "apoli:give",
	"stack": {
		"item": "minecraft:iron_axe"
	},
	"item_action": {
		"type": "apoli:damage",
		"amount": 20,
		"ignore_unbreaking": true
	},
	"preferred_slot": "offhand"
}
```

This example will give the entity an Iron Axe that has a `Damage` value of `20` that will be preferably put in the offhand equipment slot.
