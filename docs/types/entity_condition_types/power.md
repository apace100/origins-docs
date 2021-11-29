---
title: Power (Entity Condition Type)
date: 2021-04-04
---

# Power

[Entity Condition Type](../entity_condition_types.md)

Checks whether the entity has a specified power. Mostly used for [Origin conditions in layers](../../guides/data/origin_conditions_in_layers.md)

Type ID: `origins:power`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`power` | [Identifier](../data_types/identifier.md) | | The namespace and ID of the power the entity needs to have to pass the check.


### Examples

```json
"condition": {
    "type": "origins:power",
    "power": "origins:damage_from_potions"
}
```

This example will check if the player has the [`origins:damage_from_potions`](https://github.com/apace100/origins-fabric/blob/master/src/main/resources/data/origins/powers/damage_from_potions.json) power in its origin.
