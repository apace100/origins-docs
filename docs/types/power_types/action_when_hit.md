---
title: Action When Hit (Power Type)
date: 2021-10-06
---

# Action When Hit

[Power Type](../power_types.md)

Executes an action if the entity that has the power has been hit by another entity.

Type ID: `origins:action_when_hit`

!!! note

    In the context of this power type, the '**actor**' entity is the entity that did the attacking whilst the '**target**' entity is the entity that has the power.


### Fields

Field | Type | Default | Description
------|------|---------|-------------
`bientity_action` | [Bi-entity Action Type](../bientity_action_types.md) | | The action to be executed on either or both the '**actor**' and '**target**' entities.
`bientity_condition` | [Bi-entity Condition Type](../bientity_condition_types.md) | _optional_ | If specified, the specified action will only be executed if this condition is fulfilled by either or both '**actor**' and '**target**' entities.
`damage_condition` | [Damage Condition Type](../damage_condition_types.md) | _optional_ | If specified, the specified action will only be executed if this condition is fulfilled by the damage dealt by the '**actor**' entity.
`cooldown` | [Integer](../data_types/integer.md) | `1` | Interval of ticks this power needs to recharge before the power can be triggered again.
`hud_render`| [Hud Render](../data_types/hud_render.md) | `{"should_render": false}` | Determines how the cooldown of this power is visualized on the HUD.


### Examples

```json
{
    "type": "origins:action_when_hit",
    "bientity_action": {
        "type": "origins:damage",
        "amount": 2,
        "source": {
            "name": "thorns"
        }
    }
}
```

This example will deal 1 heart of damage to any entities that attacks the entity that has the power, quite similar to having an armor item that has the Thorns enchantment
