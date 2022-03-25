---
title: Action On Hit (Power Type)
date: 2021-10-06
---

# Action On Hit

[Power Type](../power_types.md)

Executes a [Bi-entity Action Type](../bientity_action_types.md) when the entity that has the power has hit another entity.

Type ID: `apoli:action_on_hit`


### Fields

Field | Type | Default | Description
------|------|---------|-------------
`bientity_action` | [Bi-entity Action Type](../bientity_action_types.md) | | The action to be executed on either or both 'actor' (the entity that has the power) and 'target' (the entity/entities that's been hit) entities.
`damage_condition` | [Damage Condition Type](../damage_condition_types.md) | _optional_ | If specified, the action will only execute when this condition holds for the damage that was dealt by the 'actor' (the entity that has the power) entity.
`cooldown` | [Integer](../data_types/integer.md) | `1` | Interval of ticks this power needs to recharge before the power can be triggered again.
`hud_render` | [Hud Render](../data_types/hud_render.md) | `{"should_render": false}` | Determines how the cooldown of this power is visualized on the HUD.
`bientity_condition` | [Bi-entity Condition Type](../bientity_condition_types.md) | _optional_ | If specified, the action will only execute when this condition is fulfilled by either or both 'actor' (the entity that has the power) and 'target' (the entity/entities that's been hit) entities. 


### Examples

```json
{
    "type": "apoli:action_on_hit",
    "bientity_action": {
        "type": "apoli:add_velocity",
        "z": 2
    }
}
```

This example will add positive-Z axis velocity to the entity that's been hit by the entity that has the power, essentially granting the entity with this power extra knockback.
