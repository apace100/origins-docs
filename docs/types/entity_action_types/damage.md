---
title: Damage (Entity Action Type)
date: 2021-04-05
---

# Damage

[Entity Action Type](../entity_action_types.md)

Applies damage to an entity.

Type ID: `origins:damage`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`amount` | [Float](../data_types/float.md) |  | The amount of damage to deal.
`source` | [Damage Source](../data_types/damage_source.md) | **DEPRECATED** | Use `damage_type` instead. [More information here](https://gist.github.com/apace100/bfbf82a8f9d6bd2db13e4feaf653a6b0).
`damage_type` | [Identifier](../data_types/identifier.md) | | The damage type to be used. Controls e.g. the death message, invulnerabilities (e.g. towards fire), or whether armor is taken into account.


### Examples

```json
"entity_action": {
    "type": "origins:damage",
    "amount": 4,
    "damage_type": "minecraft:on_fire"
}
```

This example will deal 2 hearts of `on_fire` damage, which by its tags in vanilla is considered fire damage and bypasses armor.
