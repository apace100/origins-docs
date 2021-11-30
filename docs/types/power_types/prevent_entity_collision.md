---
title: Prevent Entity Collision (Power Type)
date: 2021-11-30
---

# Prevent Entity Collision

[Power Type](../power_types.md)

Prevents an entity colliding with the entity who has this power, if all conditions are met. 

Type ID: `origins:prevent_entity_collision`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`bientity_condition` | [Bi-entity Condition Type](../bientity_condition_types.md) | _optional_ | If specified, collision is only affected as long as both the 'actor' (the entity with the power), and the 'target' fulfill the specified conditions..


### Examples

```json
{
    "type": "origins:prevent_entity_collision",
    "bientity_condition": {
        "type": "origins:attacker"
    }
}
```

This example will cause the entity with the power to not push or be pushed by its attackers.
