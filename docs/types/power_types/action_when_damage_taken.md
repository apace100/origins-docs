---
title: Action When Damage Taken (Power Type)
date: 2021-10-06
---

# Action When Damage Taken

[Power Type](../power_types.md)

Executes an [Entity Action Type](../entity_action_types.md) on the entity that has the power if the entity has taken damage.

Type ID: `origins:action_when_damage_taken`


### Fields

Field | Type | Default | Description
------|------|---------|-------------
`entity_action` | [Entity Action Type](../entity_action_types.md) | | The action to be executed upon taking damage.
`damage_condition` | [Damage Condition Type](../damage_condition_types.md) | _optional_ | If specified, the action will only trigger when this condition holds for the specified type of damage.
`cooldown` | [Integer](../data_types/integer.md) | | Interval of ticks this power needs to recharge before the power can be triggered again.
`hud_render` | [Hud Render](../data_types/hud_render.md) | `{"should_render": false}` | Determines how the cooldown of this power is visualized on the HUD.


### Examples

```json
{
    "type": "origins:action_when_damage_taken",
    "entity_action": {
        "type": "origins:execute_command",
        "command": "say ow! i'm burning!"
    },
    "damage_condition": {
        "type": "origins:in_tag",
        "tag": "minecraft:is_fire"
    },
    "cooldown": 1
}
```

This example will execute an [Execute Command (Entity Action Type)](../entity_action_types/execute_command.md) that will execute a `/say` command that will display a "`[ENTITYNAME] ow! i'm burning!`" in chat if the entity has taken fire-related damage type.
