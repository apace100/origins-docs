---
title: Damage (Bi-entity Action Type)
date: 2021-12-06
---

# Damage

[Bi-entity Action Type](../bientity_action_types.md)

Applies damage to the target entity as if the actor entity has attacked it.

Type ID: `origins:damage`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`amount` | [Float](../data_types/float.md) | | The amount of damage to deal.
`source` | [Damage Source](../data_types/damage_source.md) | **DEPRECATED** | Use `damage_type` instead. [More information here](https://gist.github.com/apace100/bfbf82a8f9d6bd2db13e4feaf653a6b0).
`damage_type` | [Identifier](../data_types/identifier.md) | | The damage type to be used. Controls e.g. the death message, invulnerabilities (e.g. towards fire), or whether armor is taken into account.


### Examples

```json
"bientity_action": {
    "type": "origins:damage",
    "amount": 10,
    "damage_type": "minecraft:cramming"
}
```

This example will deal 5 hearts of `cramming` damage to the target as if the actor has hit them, and that, if killed, will display a *"`<targetName>` was squashed by `<actorName>`",* where `<targetName>` is the name of the target and `<actorName>` is the name of the actor.
