---
title: XP Points (Entity Condition Type)
date: 2021-04-04
---

# XP Points

[Entity Condition Type](../entity_condition_types.md)

Checks the experience points of the entity.

Type ID: `origins:xp_points`

!!! note

    **This entity condition type will only work on players.**


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`comparison` | [Comparison](../data_types/comparison.md) | | Determines how the experience points of the player should be compared to the specified value.
`compare_to` | [Integer](../data_types/integer.md) | | The value at which the experience points of the player will be compared to.


### Examples

```json
"condition": {
    "type": "origins:xp_points",
    "comparison": ">=",
    "compare_to": 90
}
```

This example will check if the player has 90 or more experience points, which is only achieveable if the player have at least 7 levels.
