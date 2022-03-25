---
title: XP Levels (Entity Condition Type)
date: 2021-04-04
---

# XP Levels

[Entity Condition Type](../entity_condition_types.md)

Checks the current experience level of the entity.

Type ID: `apoli:xp_levels`

!!! note

    **This entity condition type will only work on players.**


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`comparison` | [Comparison](../data_types/comparison.md) | | How the experience level of the player should be compared to the specified value.
`compare_to` | [Integer](../data_types/integer.md) | | Which value the experience level should be compared to.


### Examples

```json
"condition": {
    "type": "apoli:xp_levels",
    "comparison": "<=",
    "compare_to": 5
}
```

This example will check if the player has 5 levels or less.
