---
title: Fall Distance (Entity Condition Type)
date: 2021-04-04
---

# Fall Distance

[Entity Condition Type](../entity_condition_types.md)

Checks how much blocks the entity has been falling.

Type ID: `origins:fall_distance`

!!! note

    This entity condition type will return `0` if the entity has the Slow Falling status effect.


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`comparison` | [Comparison](../data_types/comparison.md) | | How the fall distance should be compared to the specified value.
`compare_to` | [Float](../data_types/float.md) | | The value to compare the fall distance to.


### Examples

```json
"condition": {
    "type": "origins:fall_distance",
    "comparison": ">=",
    "compare_to": 4
}
```

This example will check if the entity has been falling for 4 or more blocks.
