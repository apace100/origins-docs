---
title: Conditioned Restrict Armor (Power Type)
date: 2021-07-04
---

# Conditioned Restrict Armor

[Power Type](../power_types.md)

Restricts the entity that has the power from equipping items as armor (via right-click, dispensing or by dragging and dropping the item in the equipment slot(s)) in the specified equipment slot(s); may depend on a `condition`.

Type ID: `origins:conditioned_restrict_armor`

!!! note

    You can use the [Restrict Armor](restrict_armor.md) power type if an entity condition is not needed.

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`head` | [Item Condition](../item_conditions.md) | _optional_ | If specified, items which fulfills this condition cannot be equipped in the head equipment slot.
`chest` | [Item Condition](../item_conditions.md) | _optional_ | If specified, items which fulfills this condition cannot be equipped in the chest equipment slot.
`legs` | [Item Condition](../item_conditions.md) | _optional_ | If specified, items which fulfills this condition cannot be equipped in the legs equipment slot.
`feet` | [Item Condition](../item_conditions.md) | _optional_ | If specified, items which fulfills this condition cannot be equipped in the feet equipment slot.
`tick_rate` | [Integer](../data_types/integer.md) | `80` | The frequency (in ticks) with which to check the condition. Lower values mean the condition changes are detected more quickly, but this comes at a potentially huge performance cost.

### Example
```json
{
  	"type": "origins:conditioned_restrict_armor",
  	"head": {
    	"type": "origins:armor_value",
    	"comparison": ">",
    	"compare_to": 2
  	},
  	"chest": {
    	"type": "origins:armor_value",
    	"comparison": ">",
    	"compare_to": 5
  	},
  	"legs": {
    	"type": "origins:armor_value",
    	"comparison": ">",
    	"compare_to": 4
  	},
  	"feet": {
    	"type": "origins:armor_value",
    	"comparison": ">",
    	"compare_to": 1
	},
	"condition": {
		"type": "origins:in_block",
		"block_condition": {
			"type": "origins:light_level",
			"comparison": ">",
			"compare_to": 6
		}
	},
	"tick_rate": 20
}
```
This power prevents the player from putting on any armor which is more powerful than chainmail, unless they are in dark places (light level below 7).
