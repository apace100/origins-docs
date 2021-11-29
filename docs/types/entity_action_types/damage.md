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
`source` | [Damage Source](../data_types/damage_source.md) |  | The damage source to be used. Controls e.g. the death message, invulnerabilities (e.g. towards fire), or whether armor is taken into account.


### Examples

```json
"entity_action": {
    "type": "origins:damage",
    "amount": 4,
    "source": {
        "name": "onFire",
        "fire": true,
        "bypasses_armor": true
    }
}
```

This example will deal 2 hearts of `onFire` damage that is considered as fire damage, and bypasses armor.
