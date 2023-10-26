---
title: Climbing (Power Type)
date: 2021-04-08
---

# Climbing

[Power Type](../power_types.md)

Allows the entity that has the power to climb.

Type ID: `origins:climbing`

!!! note

    To have the usual climbing effect, it is recommended to check for the [Collided Horizontally (Entity Condition Type)](../entity_condition_types/collided_horizontally.md) inside the `condition` object of the power.


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`allow_holding` | [Boolean](../data_types/boolean.md) | `true` | If `true`, the entity that has the power is able to hold onto blocks.
`hold_condition` | [Entity Condition Type](../entity_condition_types.md) | _optional_ | If specified and `allow_holding` is `true`, the entity that has the power will be able to 'hold onto the block' (not affected by gravity) if this condition is fulfilled, otherwise, defaults to if the entity is sneaking.


### Examples

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

This example will allow the entity to climb in cobwebs and hold onto them by sneaking.
