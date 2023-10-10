---
title: Action On Death (Power Type)
date: 2023-10-09
---

# Action On Death

[Power Type](../power_types.md)

Executes an action when the entity that has the power dies.

Type ID: `origins:action_on_death`

!!! note

    In the context of this power type, the '**target**' entity is the entity that died while the '**actor**' entity is the one that killed it.


### Fields

Field | Type | Default | Description
------|------|---------|-------------
`bientity_action` | [Bi-entity Action Type](../bientity_action_types.md) | | The action to be executed on either or both the '**actor**' and '**target**' entities.
`bientity_condition` | [Bi-entity Condition Type](../bientity_condition_types.md) | _optional_ | If specified, the specified action will only be executed if this condition is fulfilled by either or both '**actor**' and '**target**' entities.
`damage_condition` | [Damage Condition Type](../damage_condition_types.md) | _optional_ | If specified, the specified action will only be executed if this condition is fulfilled by the damage dealt by the '**actor**' entity.


### Examples

```json
{
    "type": "origins:action_on_death",
    "bientity_action": {
        "type": "origins:and",
        "actions": [
            {
                "type": "origins:target_action",
                "action": {
                    "type": "origins:explode",
                    "power": 5,
                    "destruction_type": "none",
                    "damage_self": false
                }
            }
        ]
    }
}
```

This example will make the entity that died explode.
