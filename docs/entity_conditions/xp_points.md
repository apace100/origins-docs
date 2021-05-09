---
title: XP Points
date: 2021-04-04
---
# XP Points

[Entity Condition](../entity_conditions.md).

Checks the experience points of the player.

Type ID: `origins:xp_points`

### Fields:

Field  | Type | Default | Description
-------|------|---------|-------------
`comparison` | [Comparison](../data_types/comparison.md) | | How the experience points of the player should be compared to the specified value.
`compare_to` | [Integer](../data_types/integer.md) | | Which value the experience points should be compared to.

### Example:
```json
"condition": {
    "type": "origins:xp_points",
    "comparison": ">=",
    "compare_to": 90
}
```
This example checks if the player has 90 or more experience points, which is only achieveable if the player have at least 7 levels.