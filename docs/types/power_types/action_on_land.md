---
title: Action On Land (Power Type)
date: 2021-04-04
---

# Action On Land

[Power Type](../power_types.md)

Executes an [Entity Action Type](../entity_action_types.md) when the player lands on the ground after being airborne.

Type ID: `origins:action_on_land`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`entity_action` | [Entity Action Type](../entity_action_types.md) | | The action to execute on the player.



### Examples

```json
{
    "type": "origins:action_on_land",
    "entity_action": {
        "type": "origins:execute_command",
        "command": "fill ~1 ~-1 ~1 ~-1 ~-1 ~-1 minecraft:air replace minecraft:grass_block"
    },
    "condition": {
        "type": "origins:fall_distance",
        "comparison": ">",
        "compare_to": 4
    }
}
```

This example will execute an [Execute Command (Entity Action Type)](../entity_action_types/execute_command.md) that will then execute a `/fill` command that will replace a 3x3 area of Grass Blocks with Air underneath the entity's feet if the entity in question has been falling for 4 or more blocks.
