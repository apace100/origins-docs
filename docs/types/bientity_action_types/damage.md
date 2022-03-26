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
`source` | [Damage Source](../data_types/damage_source.md) | | The damage source to be used. Controls e.g. the death message, invulnerabilities (e.g. towards fire), or whether armor is taken into account.


### Examples

```json
"bientity_action": {
    "type": "origins:damage",
    "amount": 10,
    "source": {
        "name": "cramming.player",
        "bypasses_armor": true
    }
}
```

This example will deal a `cramming.player` 5 hearts of damage to the target as if the actor has hit them, and that, if killed, will display a *"`<targetName>` was squashed by `<actorName>`",* where `<targetName>` is the name of the target and `<actorName>` is the name of the actor.
