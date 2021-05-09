---
title: Attacker (Condition)
date: 2021-04-04
---
# Attacker

[Damage Condition](../damage_conditions.md).

Checks whether the condition has an attacker, and optionally whether the attacker fulfills a specified [Entity Condition](../entity_conditions.md).

Type ID: `origins:attacker`

### Fields:

Field  | Type | Default | Description
-------|------|---------|-------------
`entity_condition` | [Entity Condition](../entity_conditions.md) | _optional_ | If set, the attacking entity must fulfill the provided entity condition in order for this condition to evaluate to true.

### Example
```json
"damage_condition": {
    "type": "origins:attacker",
    "entity_condition": {
        "type": "origins:entity_type",
        "entity_type": "minecraft:zombie"
    }
}
```
This example checks if the attacker is a Zombie using the [`origins:entity_type`](../entity_conditions/entity_type.md) entity condition type.