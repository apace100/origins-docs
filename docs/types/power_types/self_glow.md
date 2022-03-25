---
title: Self Glow (Power Type)
date: 2021-10-06
---

# Self Glow

[Power Type](../power_types.md)

Makes the entity that has the power glow if certain conditions are met.

Type ID: `apoli:self_glow`


### Fields

Field | Type | Default | Description
------|------|---------|-------------
`entity_condition` | [Entity Condition Type](../entity_condition_types.md) | _optional_ | If specified, only entities that fulfills this condition will see the entity that has the power glow.
`bientity_condition` | [Bi-entity Condition Type](../bientity_condition_types.md) | _optional_ | If set, only entities which fulfill this bi-entity condition in relation to the entity that has the power will see the entity that has the power glow.
`use_teams` | [Boolean](../data_types/boolean.md) | `true` | Determines whether glowing entities should use their team's color with their glow. If set to false, the entity will instead use the `red`, `green` and `blue` fields within this power type.
`red` | [Float](../data_types/float.md) | `1.0` | Value by which the red component of the glow will be multiplied. Range: 0.0 - 1.0.
`green` | [Float](../data_types/float.md) | `1.0` | Value by which the green component of the glow will be multiplied. Range: 0.0 - 1.0.
`blue` | [Float](../data_types/float.md) | `1.0` | Value by which the blue component of the glow will be multiplied. Range: 0.0 - 1.0.


### Examples

```json
{
    "type": "apoli:self_glow",
    "use_teams": false,
    "red": 0.56862745098,
    "green": 0.89019607843,
    "blue": 0.65098039215,
    "condition": {
        "type": "apoli:in_rain"
    }
}
```

This example will make the entity that has the power glow for everyone if the entity in question is in rain.
<br>

```json
{
    "type": "apoli:self_glow",
    "bientity_condition": {
        "type": "apoli:can_see"
    },
    "use_teams": false,
    "red": 1.0,
    "green": 0.0,
    "blue": 0.0
}
```

This example will make the entity that has the power glow for the entity that can see the said entity.
