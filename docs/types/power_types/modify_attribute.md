---
title: Modify Attribute (Power Type)
date: 2022-07-03
---

#   Modify Attribute

[Power Type](../power_types.md)

Modifies an attribute using [Attribute Modifiers](../data_types/attribute_modifier.md).

Type ID: `origins:modify_attribute`

!!! note

    This power type uses a different modifier system than the [Attribute (Power Type)](attribute.md) and the [Conditioned Attribute (Power Type)](conditioned_attribute.md).

!!! note

    Refer to the [Minecraft Fandom Wiki: Attribute](https://minecraft.fandom.com/wiki/Attribute) page for a list of **vanilla** attributes that you can modify.


### Fields

Field | Type | Value | Description
------|------|-------|------------
`attribute` | [Identifier](../data_types/identifier.md) | | The namespace and ID of the attribute to apply the modifier(s) to.
`modifier` | [Attribute Modifier](../data_types/attribute_modifier.md) | _optional_ | If specified, this modifier will be applied to the specified attribute.
`modifiers` | [Array](../data_types/array.md) of [Attribute Modifiers](../data_types/attribute_modifier.md) | _optional_ | If specified, these modifiers will be applied to the specified attribute.


### Examples

```json
{
    "type": "origins:modify_attribute",
    "attribute": "minecraft:generic.attack_damage",
    "modifier": {
        "operation": "set_total",
        "resource": "example:resource",
        "value": 0
    }
}
```

This example will set the total value of the entity's `minecraft:generic.attack_damage` attribute using the value of the `example:resource` (`data/example/powers/resource.json`) power.
