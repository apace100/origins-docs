---
title: Conditioned Restrict Armor (Power Type)
date: 2021-07-04
---

# Conditioned Restrict Armor

[Power Type](../power_types.md)

Restricts the entity that has the power from equipping items as armor (via right-click, dispensing or by dragging and dropping the item in the equipment slot(s)) in the specified equipment slot(s); may depend on a `condition`.

Type ID: `apoli:conditioned_restrict_armor`

!!! note

    You can use the [Restrict Armor (Power Type)](restrict_armor.md) if an entity condition is not needed.


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`head` | [Item Condition Type](../item_condition_types.md) | _optional_ | If specified, items which fulfills this condition cannot be equipped in the head equipment slot.
`chest` | [Item Condition Type](../item_condition_types.md) | _optional_ | If specified, items which fulfills this condition cannot be equipped in the chest equipment slot.
`legs` | [Item Condition Type](../item_condition_types.md) | _optional_ | If specified, items which fulfills this condition cannot be equipped in the legs equipment slot.
`feet` | [Item Condition Type](../item_condition_types.md) | _optional_ | If specified, items which fulfills this condition cannot be equipped in the feet equipment slot.
`tick_rate` | [Integer](../data_types/integer.md) | `80` | The frequency (in ticks) with which to check the condition. Lower values mean the condition changes are detected more quickly, but this comes at a potentially huge performance cost.


### Examples

```json
{
  	"type": "apoli:conditioned_restrict_armor",
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
	},
	"condition": {
		"type": "apoli:in_block",
		"block_condition": {
			"type": "apoli:light_level",
			"comparison": ">",
			"compare_to": 6
		}
	},
	"tick_rate": 20
}
```

This example will prevent the entity from equipping any armor which is more powerful than chainmail, unless the entity is in dark places (light level below 7).
