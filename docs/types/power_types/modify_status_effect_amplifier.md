---
title: Modify Status Effect Amplifier (Power Type)
date: 2021-12-04
---

# Modify Status Effect Amplifier

[Power Type](../power_types.md)

Modifies the amplifier of the specified status effect upon receiving the specified status effect.

Type ID: `origins:modify_status_effect_amplifier`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`status_effect` | [Identifier](../data_types/identifier.md) | | The namespace and ID of the status effect that will have its amplifier modified.
`modifier` | [Attribute Modifier](../data_types/attribute_modifier.md) | | The modifier to apply to the amplifier of the specified status effect.


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

This example will modify the amplifier of the Speed status effect to have a 1 level increase, making the entity that has the power recieve Speed II if the entity were to receive Speed I, etc.
