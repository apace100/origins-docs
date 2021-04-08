---
title: Damage (Action)
date: 2021-04-05
---
# Damage

[Entity Action](../entity_actions.md).

Applies damage to an entity.

Type ID: `origins:damage`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`amount` | [Float](../data_types/float.md) |  | The amount of damage to deal.
`source` | [Damage Source](../data_types/damage_source.md) |  | The damage source to be used. Controls e.g. the death message, invulnerabilities (e.g. towards fire), or whether armor is taken into account.

### Example
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
This action deals 2 hearts of damage as if the target was burning.
