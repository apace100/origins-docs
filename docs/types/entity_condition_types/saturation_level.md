---
title: Saturation Level (Entity Condition Type)
date: 2021-04-04
---

# Saturation Level

[Entity Condition Type](../entity_condition_types.md)

Checks the entity's saturation level, which is the invisible value that determines how "full" the entity is, which then determines how long it takes before the hunger level of the entity will go down.

Type ID: `origins:saturation_level`

!!! note

    **This entity condition type will only work on players.**


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`comparison` | [Comparison](../data_types/comparison.md) | | Determines how the saturation level of the player should be compared to the specified value.
`compare_to` | [Float](../data_types/float.md) | | The value at which the saturation level of the player will be compared to.


### Examples

```json
"condition": {
    "type": "origins:saturation_level",
    "comparison": "==",
    "compare_to": 0
}
```

This example will check if the player's saturation level reaches 0.
