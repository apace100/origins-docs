---
title: Air (Condition)
date: 2021-04-04
---
# Air

[Entity Condition](../entity_conditions.md).

Checks how much breath / air / bubbles the player has at the moment.

Type ID: `origins:air`

### Fields:

Field  | Type | Default | Description
-------|------|---------|-------------
`comparison` | [Comparison](../data_types/comparison.md) | |  How the breath (in ticks) should be compared to the specified value.
`compare_to` | [Integer](../data_types/integer.md) | | Which value the breath should be compared to.

### Example:
```json
"condition": {
    "type": "origins:air",
    "comparison": "==",
    "compare_to": 0
}
```
This example would check if the player has no air / bubbles left.