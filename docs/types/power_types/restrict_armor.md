---
title: Restrict Armor (Power Type)
date: 2021-04-07
---

# Restrict Armor

[Power Type](../power_types.md)

Restricts the entity that has the power from equipping items as armor (via right-click, dispensing or by dragging and dropping the item in the equipment slot(s)) in the specified equipment slot(s).

Type ID: `apoli:restrict_armor`

!!! note

	This power type does not support a `condition`. If the `condition` field is present, it will be ignored. If you wish to check for an entity condition before applying the restriction, you can use the [Conditioned Restrict Armor](conditioned_restrict_armor.md) power type instead.


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`head` | [Item Condition Type](../item_condition_types.md) | _optional_ | If specified, items which fulfills this condition cannot be equipped in the head equipment slot.
`chest` | [Item Condition Type](../item_condition_types.md) | _optional_ | If specified, items which fulfills this condition cannot be equipped in the chest equipment slot.
`legs` | [Item Condition Type](../item_condition_types.md) | _optional_ | If specified, items which fulfills this condition cannot be equipped in the legs equipment slot.
`feet` | [Item Condition Type](../item_condition_types.md) | _optional_ | If specified, items which fulfills this condition cannot be equipped in the feet equipment slot.


### Examples

```json
{
	"type": "apoli:restrict_armor",
	"head": {
		"type": "apoli:armor_value",
		"comparison": ">",
		"compare_to": 2
	},
	"chest": {
		"type": "apoli:armor_value",
		"comparison": ">",
		"compare_to": 5
	},
	"legs": {
		"type": "apoli:armor_value",
		"comparison": ">",
		"compare_to": 4
	},
	"feet": {
		"type": "apoli:armor_value",
		"comparison": ">",
		"compare_to": 1
	}
}
```

This example will prevent the entity from equipping any armor which has more defense than chainmail.

```json
{
    "type": "apoli:restrict_armor",
    "chest": {
        "type": "apoli:ingredient",
        "ingredient": {
            "item": "minecraft:turtle_helmet"
        }
    },
    "chest": {
        "type": "apoli:ingredient",
        "ingredient": {
            "item": "minecraft:elytra"
        }
    }
}
```

This example will prevent the entity from equipping a Turtle Shell or an Elytra.
