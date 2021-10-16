---
title: Give (Entity Action)
date: 2021-04-06
---
# Give

[Entity Action](../entity_actions.md).

Gives the entity an item stack, by inserting it into its inventory or dropping it on the ground if there is no available space.

Type ID: `origins:give`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`stack` | [Item Stack](../data_types/item_stack.md) |  | The item stack to give to the entity.
`item_action` | [Item Action](../item_actions.md) | _optional_ | If set, executes an item action on the item stack before it's given to the player.
`preferred_slot` | [String](../data_types/string.md) | _optional_ | If set, this will prioritize the action to put the item in the specified slot. Accepts `"chest"`, `"feet"`, `"head"`, `"legs"`, `"mainhand"` or `"offhand"`.

### Examples
```json
"entity_action": {
  	"type": "origins:give",
  	"stack": {
	  "item": "minecraft:egg",
	  "amount": 3
  	}
}
```
Gives the entity a stack of 3 eggs.
<br>

```json
"entity_action": {
    "type": "origins:give",
    "stack": {
        "type": "minecraft:iron_axe"
    },
    "item_action": {
        "type": "origins:damage",
        "amount": 20,
        "ignore_unbreaking": true
    },
    "preferred_slot": "offhand"
}
```
This example gives the player an iron axe that has a `Damage` value of 20 that will be preferably put in the offhand slot.