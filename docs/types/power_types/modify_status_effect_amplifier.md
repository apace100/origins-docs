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
`status_effect` | [Identifier](../data_types/identifier.md) | _optional_ | If specified, only this status effect will have its amplifier modified upon being received.
`status_effects` | [Array](../data_types/array.md) of [Identifiers](../data_types/identifier.md) | _optional_ | If specified, only these status effect(s) will have its amplifier modified upon being received.
`modifier` | [Attribute Modifier](../data_types/attribute_modifier.md) | _optional_ | If specified, this modifier will be applied to the amplifier of the specified status effect(s).
`modifiers` | [Array](../data_types/array.md) of [Attribute Modifiers](../data_types/attribute_modifier.md) | _optional_ | If specified, these modifiers will be applied to the amplifier of the specified status effect(s).


### Examples

```json
{
    "type": "origins:modify_status_effect_amplifier",
    "status_effect": "minecraft:speed",
    "modifier": {
        "operation": "add_base_early",
        "value": 1
    }
}
```

This example will modify the amplifier of the Speed status effect to have a 1 level increase, making the entity that has the power receive Speed II if the entity were to receive Speed I, etc.
