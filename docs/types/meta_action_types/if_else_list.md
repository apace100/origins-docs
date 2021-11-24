---
title: If-Else List (Meta Action Type)
date: 2021-04-07
---

# If-Else List

[Meta Action Type](../meta_action_types.md)

Checks a list of actions associated with conditions, and executes the first one in the list for which the condition holds. Basically a less indentation-heavy way to represent a deeply nested [If-Else Action](if_else.md).

Type ID: `origins:if_else_list`

!!! note

    **Currently only available as an [Entity Action](../entity_actions.md)**

!!! note

    Depending on the condition type, a different action type is expected:
    
    Action Type | Condition Type
    ------------|----------------
    [Entity Action](../entity_actions.md) | [Entity Condition](../entity_conditions.md)
    [Block Action](../block_actions.md) | [Block Condition](../block_conditions.md)
    [Item Action](../item_actions.md) | [Item Condition](../item_conditions.md)

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`actions` | [Array](../data_types/array.md) of [Objects](../data_types/object.md) | | Each object has to have an `action` [Action](../action_types.md) object and a `condition` [Condition](../condition_types.md) object.

### Example

```json
"entity_action": {
	"type": "origins:if_else_list",
	"actions": [
		{
			"condition": {
				"type": "origins:health",
				"comparison": "<=",
				"compare_to": 6
			},
			"action": {
				"type": "origins:apply_effect",
				"effect": {
					"effect": "minecraft:speed",
					"amplifier": 2,
					"duration": 80
				}
			}
		},
		{
			"condition": {
				"type": "origins:health",
				"comparison": "<=",
				"compare_to": 12
			},
			"action": {
				"type": "origins:apply_effect",
				"effect": {
					"effect": "minecraft:speed",
					"amplifier": 1,
					"duration": 80
				}
			}
		},
		{
			"condition": {
				"type": "origins:health",
				"comparison": "<=",
				"compare_to": 18
			},
			"action": {
				"type": "origins:apply_effect",
				"effect": {
					"effect": "minecraft:speed",
					"amplifier": 0,
					"duration": 80
				}
			}
		}
	]
}
```
This action will apply a stronger speed effect the lower the entity's health is, in three stages (<= 3 hearts, <= 6 hearts or <= 9 hearts).
