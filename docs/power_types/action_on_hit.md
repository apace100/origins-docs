---
title: Action On Hit (Power Type)
date: 2021-10-06
---
# Action On Hit

[Power Type](../power_types.md)

Executes a bi-entity action that can execute on the entity that has the power, the entity that has been hit or both if the entity that has the power has hit another entity.

Type ID: `origins:action_on_hit`

### Fields

Field | Type | Default | Description
------|------|---------|-------------
`bientity_action` | [Bi-entity Action](../bientity_actions.md) | | Execute the specified bi-entity action.
`damage_condition` | [Damage Condition](../damage_conditions.md) | _optional_ | If set, the action will only trigger when this condition holds for the damage that was dealt by the entity that has the power.
`cooldown` | [Integer](../data_types/integer.md) | 1 | Interval of ticks this power needs to recharge before the action can be executed again.
`hud_render` | [Hud Render](../data_types/hud_render.md) | `{"should_render": false}` | Determines how the cooldown of this power is visualized on the HUD.
`bientity_condition` | [Bi-entity Condition](../bientity_conditions.md) | If set, the action will only trigger when this bi-entity condition is fulfilled.

### Example
```json
{
    "type": "origins:action_on_hit",
    "bientity_action": {
        "type": "origins:add_velocity",'
        "z": 2
    }
}
```
This example adds velocity to the entity that's been hit by the entity that has the power, essentially granting the entity with this power extra knockback.