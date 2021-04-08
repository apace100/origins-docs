---
title: Climbing (Power Type)
date: 2021-04-08
---
# Climbing

[Power Type](../power_types.md).

Allows players to climb.

**Note**: Keep in mind that the climbing is performed always while this power is active. Thus, a condition which checks for a horizontal collision is required for the player to have the usual climbing effect.

Type ID: `origins:climbing`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`allow_holding` | [Boolean](../data_types/boolean.md) | true | If true, the player is able to hold onto blocks.
`hold_condition` | [Entity Condition](../entity_conditions.md) | _optional_ | If set and `allow_holding` is true, players with the power who are sneaking and meet this condition are "holding onto the block", meaning they won't be affected by gravity.

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
