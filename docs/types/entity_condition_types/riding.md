---
title: Riding (Entity Condition Type)
date: 2021-10-07
---

# Riding

[Entity Condition Type](../entity_condition_types.md)

Checks whether the '**actor**' entity is directly riding the '**target**' entity.

Type ID: `origins:riding`


!!! note

    In the context for this entity condition type, the '**actor**' entity is the passenger and the entity that invoked the condition while the '**target**' entity is the entity that is being ridden.


### Fields

Field | Type | Default | Description
------|------|---------|-------------
`bientity_condition` | [Bi-entity Condition Type](../bientity_condition_types.md) | _optional_ | If specified, this condition type will only evaluate to true if this condition is fulfilled by either or both the '**actor**' and '**target**' entities.


### Examples

```json
"condition": {
    "type": "origins:riding"
}
```

This example will check if the '**actor**' entity is riding an entity.
<br>


```json
"condition": {
    "type": "origins:riding",
    "bientity_condition": {
        "type": "origins:target_condition",
        "condition": {
            "type": "origins:entity_type",
            "entity_type": "minecraft:minecart"
        }
    }
}
```

This example will check if the '**actor**' entity is currently riding a minecart ('**target**' entity).
