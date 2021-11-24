---
title: Climbing (Power Type)
date: 2021-04-08
---

# Climbing

[Power Type](../power_types.md)

Allows the entity that has the power to climb.

Type ID: `origins:climbing`

!!! note

    To have the usual climbing effect, it is recommended to check for the [Collided Horizontally](../entity_conditions/collided_horizontally.md) entity condition type inside the `condition` object of the power.

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`allow_holding` | [Boolean](../types/data_types/boolean.md) | `true` | If `true`, the entity that has the power is able to hold onto blocks.
`hold_condition` | [Entity Condition](../entity_conditions.md) | _optional_ | If specified and `allow_holding` is `true`, the entity that has the power will be able to 'hold onto the block' (not affected by gravity) if the entity is sneaking and if this condition is fulfilled.

### Example
```json
{
    "type": "origins:climbing",
    "condition": {
		"type": "origins:in_block_anywhere",
		"block_condition": {
			"type": "origins:in_tag",
			"tag": "origins:cobwebs"
		}
    },
    "hold_condition": {
		"type": "origins:in_block_anywhere",
		"block_condition": {
			"type": "origins:in_tag",
			"tag": "origins:cobwebs"
		}
    }
}
```
This power allows players to climb in cobwebs, and also hold onto them by sneaking.
