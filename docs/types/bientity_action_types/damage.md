---
title: Damage (Bi-entity Action Type)
date: 2021-12-06
---

# Damage

[Bi-entity Action Type](../bientity_action_types.md)

Applies damage to the target entity as if the actor entity has attacked it.

Type ID: `origins:damage`


!!! info

    See [Minecraft Wiki: Damage type](https://minecraft.wiki/w/Damage_type) and [Minecraft Wiki: Tags (Damage types)](https://minecraft.wiki/w/Tag#Damage_types) for more information about vanilla damage types and damage type tags.


### Fields

Field | Type | Default | Description
------|------|---------|------------
`amount` | [Float](../data_types/float.md) | | The amount of damage to deal.
`source` | [Damage Source](../data_types/damage_source.md) | <span style="color:darkred"><b>DEPRECATED</b></span> | Use `damage_type` instead. See [Damage Source (Data Type)](../data_types/damage_source.md) for more details.
`damage_type` | [Identifier](../data_types/identifier.md) | | Defines the properties of the damage source that will be dealt, such as part of its death message, and whether it can bypass armor, shield, etc. (via damage type tags.)
`modifier` | [Attribute Modifier](../data_types/attribute_modifier.md) | _optional_ | If specified, this modifier will be applied to the damage taken by the '**target**' entity.
`modifiers` | [Array](../data_types/array.md) of [Attribute Modifiers](../data_types/attribute_modifier.md) | _optional_ | If specified, these modifiers will be applied to the damage taken by the '**target**' entity.


### Examples

```json
"bientity_action": {
    "type": "origins:damage",
    "amount": 10,
    "damage_type": "minecraft:cramming"
}
```

This example will deal 5 hearts of `cramming` damage to the target as if the actor has hit them, and that, if killed, will display a *"`<targetName>` was squashed by `<actorName>`",* where `<targetName>` is the name of the target and `<actorName>` is the name of the actor.
