---
title: Action When Damage Taken (Power Type)
date: 2021-10-06
---

# Action When Damage Taken

[Power Type](../power_types.md)

Executes an entity action on the entity that has the power if the entity has taken damage.

Type ID: `origins:action_when_damage_taken`

### Fields

Field | Type | Default | Description
------|------|---------|-------------
`entity_action` | [Entity Action](../entity_actions.md) | | The action to be executed upon taking damage.
`damage_condition` | [Damage Condition](../damage_conditions.md) | _optional_ | If specified, the action will only trigger when this condition holds for the specified type of damage.
`cooldown` | [Integer](../types/data_types/integer.md) | | Interval of ticks this power needs to recharge before the power can be triggered again.
`hud_render` | [Hud Render](../types/data_types/hud_render.md) | `{"should_render": false}` | Determines how the cooldown of this power is visualized on the HUD.

### Example
```json
{
    "type": "origins:action_when_damage_taken",
    "entity_action": {
        "type": "origins:execute_command",
        "command": "say ow! i'm burning!"
    },
    "damage_condition": {
        "type": "origins:fire"
    },
    "cooldown": 1
}
```
This example executes an `origins:execute_command` entity action if the damage type taken is fire-related.