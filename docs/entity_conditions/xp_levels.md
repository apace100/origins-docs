---
title: XP Levels
date: 2021-04-04
---
# XP Levels

[Entity Condition](../entity_conditions.md).

Checks the experience level of the player.

Type ID: `origins:xp_levels`

### Fields:

Field  | Type | Default | Description
-------|------|---------|-------------
`comparison` | [Comparison](../data_types/comparison.md) | | How the experience level of the player should be compared to the specified value.
`compare_to` | [Integer](../data_types/integer.md) | | Which value the experience level should be compared to.

### Example:
```json
"condition": {
    "type": "origins:xp_levels",
    "comparison": "<=",
    "compare_to": 5
}
```
This example checks if the player has 5 levels or less.