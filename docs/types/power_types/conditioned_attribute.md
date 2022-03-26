---
title: Conditioned Attribute (Power Type)
date: 2021-04-07
---

# Conditioned Attribute

[Power Type](../power_types.md)

Applies one or more attribute modifiers; may depend on a `condition`.

Type ID: `origins:conditioned_attribute`

!!! note

    You can use the [Attribute (Power Type)](attribute.md) if an entity condition is not needed.

!!! note

    Refer to the [Minecraft Fandom Wiki: Attribute](https://minecraft.fandom.com/wiki/Attribute) page for a list of **vanilla** attributes that you can modify.


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`modifier` | [Attributed Attribute Modifier](../data_types/attributed_attribute_modifier.md) | _optional_ | If specified, this modifier will be applied to its corresponding attribute.
`modifiers` | [Array](../data_types/array.md) of [Attributed Attribute Modifiers](../data_types/attributed_attribute_modifier.md) | _optional_ | If specified, these modifiers will be applied to their corresponding attributes.
`tick_rate` | [Integer](../data_types/integer.md) | `20` | The frequency (in ticks) with which to check the condition. Lower values mean the condition changes are detected more quickly, but this comes at a potentially huge performance cost.
`update_health` | [Boolean](../data_types/boolean.md) | `true` | Determines whether the health percentage will update to match the entity's new maximum health.



### Examples

```json
{
    "type": "origins:conditioned_attribute",
    "modifier": {
        "attribute": "minecraft:generic.movement_speed",
        "operation": "addition",
        "value": 0.4,
        "name": "Increased sprinting speed"
    },
    "tick_rate": 20,
    "condition": {
        "type": "origins:sprinting"
    }
}
```

This example power will add 0.4 to the entity's `minecraft:generic.movement_speed` attribute if the entity is sprinting.
