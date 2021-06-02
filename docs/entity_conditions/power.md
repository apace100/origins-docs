---
title: Power
date: 2021-04-04
---
# Power

[Entity Condition](../entity_conditions.md).

Checks whether the player has a certain power (just theoretically, it doesn't need to be active at the moment of the check). Mostly used for [Origin conditions in layers](../guides/data/origin_conditions_in_layers.md).

Type ID: `origins:power`

### Fields:

Field  | Type | Default | Description
-------|------|---------|-------------
`power` | [Identifier](../data_types/identifier.md) | |  ID of the power the player needs to have to pass the check.

### Example:
```json
"condition": {
    "type": "origins:power",
    "power": "origins:damage_from_potions"
}
```
This example checks if the player has the [`origins:damage_from_potions`](https://github.com/apace100/origins-fabric/blob/master/src/main/resources/data/origins/powers/damage_from_potions.json) power in its origin.