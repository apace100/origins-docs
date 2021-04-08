---
title: Conditioned Restrict Armor (Power Type)
date: 2021-04-07
---
# Conditioned Restrict Armor

[Power Type](../power_types.md).

Blocks the player from equipping items as armor (via right-click, from dispensing, and by dragging them over in the inventory). May depend on a condition, use [Restrict Armor](restrict_armor.md) if you are not adding a `condition` (except the item conditions, of course).

Type ID: `origins:conditioned_restrict_armor`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`head` | [Item Condition](../item_conditions.md) | _optional_ | If set, items which satisfy this condition can not be equipped in the head slot.
`chest` | [Item Condition](../item_conditions.md) | _optional_ | If set, items which satisfy this condition can not be equipped in the chest slot.
`legs` | [Item Condition](../item_conditions.md) | _optional_ | If set, items which satisfy this condition can not be equipped in the legs slot.
`feet` | [Item Condition](../item_conditions.md) | _optional_ | If set, items which satisfy this condition can not be equipped in the feet slot.

`tick_rate`, int, default = 80: _The frequency (in ticks) with which to check the condition. Lower values mean the condition changes are detected more quickly, but this comes at a potentially huge performance cost._

### Example
```json
{
  	"type": "origins:restrict_armor",
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
