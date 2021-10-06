---
title: Action When Damage Taken (Power Type)
date: 2021-10-06
---
# Action When Damage Taken

[Power Type](../power_types.md)

Executes an entity action on the player if the player in question takes damage.

Type ID: `origins:action_when_damage_taken`

### Fields

Field | Type | Default | Description
------|------|---------|-------------
`entity_action` | [Entity Action](../entity_actions.md) | | The action to be executed upon taking damage.
`damage_condition` | [Damage Condition](../damage_conditions.md) | _optional_ | If specified, the action will only trigger when this condition holds for the specified type of damage.
`cooldown` | [Integer](../data_types/integer.md) | 1 | Interval of ticks this power needs to recharge before the action can be executed again.
`hud_render` | [Hud Render](../data_types/hud_render.md) | `{"should_render": false}` | Specifies how the cooldown of this power is visualized on the HUD.

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
    }
}
```
This example executes an `origins:execute_command` entity action if the damage type taken is fire-related.