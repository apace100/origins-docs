---
title: Modify Status Effect Duration (Power Type)
date: 2021-12-04
---

# Modify Status Effect Duration

[Power Type](../power_types.md)

Modifies the duration of the specified status effect upon receiving the specified status effect.

Type ID: `origins:modify_status_effect_duration`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`status_effect` | [Identifier](../data_types/identifier.md) | | The namespace and ID of the status effect that will have its duration modified.
`modifier` | [Attribute Modifier](../data_types/attribute_modifier.md) | | The modifier to apply to the duration of the specified status effect.


### Examples

```json
{
    "type": "origins:modify_status_effect_amplifier",
    "status_effect": "minecraft:speed",
    "modifier": {
        "operation": "addition",
        "value": 1
    }
}
```

This example will modify the duration of the Speed status effect to have a 25% increase, making the entity that has the power recieve Speed that initially lasted 60 seconds now last for 75 seconds.
