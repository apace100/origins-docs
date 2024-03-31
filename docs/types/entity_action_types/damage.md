---
title: Damage (Entity Action Type)
date: 2021-04-05
---

# Damage

[Entity Action Type](../entity_action_types.md)

Applies damage to an entity.

Type ID: `origins:damage`


!!! info

    The max health of the entity will be used as the base value for the modifier(s).


!!! info

    See [Minecraft Wiki: Damage type](https://minecraft.wiki/w/Damage_type) and [Minecraft Wiki: Tags (Damage types)](https://minecraft.wiki/w/Tag#Damage_types) for more information about vanilla damage types and damage type tags.


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`amount` | [Float](../data_types/float.md) |  | The amount of damage to deal.
`source` | [Damage Source](../data_types/damage_source.md) | <span style="color:darkred"><b>DEPRECATED</b></span> | Use `damage_type` instead. See [Damage Source (Data Type)](../data_types/damage_source.md) for more details.
`damage_type` | [Identifier](../data_types/identifier.md) | | Defines the properties of the damage source that will be dealt, such as part of its death message, and whether it can bypass armor, shield, etc. (via damage type tags.)
`modifier` | [Attribute Modifier](../data_types/attribute_modifier.md) | _optional_ | If specified, this modifier will be applied to the damage taken by the entity.
`modifiers` | [Array](../data_types/array.md) of [Attribute Modifiers](../data_types/attribute_modifier.md) | _optional_ | If specified, these modifiers will be applied to the damage taken by the entity.


### Examples

```json
"entity_action": {
    "type": "origins:damage",
    "amount": 4,
    "damage_type": "minecraft:on_fire"
}
```

This example will deal 2 hearts of `on_fire` damage, which by its tags in vanilla is considered fire damage and bypasses armor.
<br>

```json
"entity_action": {
    "type": "origins:damage",
    "damage_type": "minecraft:out_of_world",
    "modifiers": [
        {
            "operation": "set_base",
            "value": 2
        },
        {
            "operation": "multiply_total_multiplicative",
            "resource": "example:damage_multiplier",
            "value": 0
        }
    ]
}
```

This example will deal `2 * (1 + example:damage_multiplier)` amount of `out_of_world` damage to the entity, with `2` used for overriding the base value for the modifiers, and the value of the `example:damage_multiplier` (`data/example/powers/damage_multipler.json`) power as the "multiplier". If the value of the said power is `3`, the amount of damage that will be dealt will be `8` (`2 * (1 + 3) = 8`.)
