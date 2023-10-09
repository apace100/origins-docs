---
title: Prevent Elytra Flight (Power Type)
date: 2021-12-06
---

# Prevent Elytra Flight

[Power Type](../power_types.md)

Prevents the entity that has the power from flying with either an Elytra item or a power that uses the [Elytra Flight (Power Type)](elytra_flight.md).

Type ID: `origins:prevent_elytra_flight`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`entity_action` | [Entity Action Type](../entity_action_types.md) | _optional_ | If specified, this action will be executed upon the entity trying to fly an Elytra/power that uses the [Elytra Flight (Power Type)](elytra_flight.md).


### Examples

```json
{
    "type": "origins:prevent_elytra_flight",
    "entity_action": {
        "type": "origins:execute_command",
        "command": "tellraw @s {\"text\": \"You cannot glide from this height!\", \"color\": \"red\"}"
    },
    "condition": {
        "type": "origins:in_block",
        "block_condition": {
            "type": "origins:height",
            "comparison": "<=",
            "compare_to": 64
        }
    }
}
```

This example will display a warning and prevent the entity that has the power from flying with an Elytra if they're at Y=64 or lower.
