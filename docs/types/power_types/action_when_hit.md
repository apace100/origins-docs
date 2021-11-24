---
title: Action When Hit (Power Type)
date: 2021-10-06
---

# Action When Hit

[Power Type](../power_types.md)

Executes a bi-entity action if the entity that has the power has been hit by another entity.

Type ID: `origins:action_when_hit`

### Fields

Field | Type | Default | Description
------|------|---------|-------------
`bientity_action` | [Bi-entity Action](../bientity_actions.md) | | The action to be executed on either or both 'actor' (the attacker entity) entity and 'target' (the entity that has the power) entity.
`damage_condition` | [Damage Condition](../damage_conditions.md) | _optional_ | If specified, the specified action will only trigger when this condition holds for the specified type of damage.
`cooldown` | [Integer](../types/data_types/integer.md) | `1` | Interval of ticks this power needs to recharge before the power can be triggered again.
`hud_render`| [Hud Render](../types/data_types/hud_render.md) | `{"should_render": false}` | Determines how the cooldown of this power is visualized on the HUD.
`bientity_condition` | [Bi-entity Condition](../bientity_conditions.md) | _optional_ | If specified, the specified action will only trigger if this condition is fulfilled by either or both 'actor' (the attacker entity) entity and 'target' (the entity that has the power) entity.

### Example
```json
{
    "type": "origins:action_when_hit",
    "bientity_action": {
        "type": "origins:actor_action",
        "action": {
            "type": "origins:damage",
            "amount": 2,
            "source": {
                "name": "thorns"
            }
        }
    }
}
```
This example will deal 1 heart of damage to any entities that attacks the entity that has the power.