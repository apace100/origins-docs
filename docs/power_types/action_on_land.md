---
title: Action On Land (Power Type)
date: 2021-04-04
---
# Action On Land

[Power Type](../power_types.md).

Executes an entity action when the player lands on the ground after being airborne.

Type ID: `origins:action_on_land`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`entity_action` | [Entity Action](../entity_actions.md) | | The action to execute on the player.


### Example
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
If a player with this power has been falling for more than 4 blocks, it'll run a `/fill` command below the player, replacing a 3x3 area of grass blocks with air.