---
title: Attacker (Damage Condition Type)
date: 2021-04-04
---

# Attacker

[Damage Condition Type](../damage_condition_types.md)

Checks whether the damage source is from an entity.

Type ID: `origins:attacker`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`entity_condition` | [Entity Condition Type](../entity_condition_types.md) | _optional_ | If set, the attacker entity must fulfill the provided entity condition type in order for this condition to evaluate to true.


### Examples

```json
"damage_condition": {
    "type": "origins:attacker",
    "entity_condition": {
        "type": "origins:entity_type",
        "entity_type": "minecraft:zombie"
    }
}
```

This example will check if the attacker is a Zombie entity, with the [Entity Type (Entity Condition Type)](../entity_condition_types/entity_type.md) condition
