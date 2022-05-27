---
title: Power (Entity Condition Type)
date: 2021-04-04
---

# Power

[Entity Condition Type](../entity_condition_types.md)

Checks whether the entity has a specified power. Mostly used for [Origin conditions in layers](../../guides/data/origin_conditions_in_layers.md)

Type ID: `origins:power`

!!! caution

    Make sure to use the [Living (Entity Condition Type)](living.md) to check if the entity is a "living entity", otherwise, the game will crash since only living entities can have powers.


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`power` | [Identifier](../data_types/identifier.md) | | The namespace and ID of the power the entity needs to have to pass the check.
`source` | [Identifier](../data_types/identifier.md) | _optional_ | If specified, the condition will check if the power is from the specified power source.


### Examples

```json
"condition": {
    "type": "origins:power",
    "power": "origins:damage_from_potions"
}
```

This example will check if the player has the [`origins:damage_from_potions`](https://github.com/apace100/origins-fabric/blob/master/src/main/resources/data/origins/powers/damage_from_potions.json) power in its origin.
