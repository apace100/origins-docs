---
title: Saturation Level
date: 2021-04-04
---
# Saturation Level

[Entity Condition](../entity_conditions.md).

Checks the player's saturation level (the invisible value of how "full" you are, i.e. how long it takes before your hunger meter actually goes down).

Type ID: `origins:saturation_level`

### Fields:

Field  | Type | Default | Description
-------|------|---------|-------------
`comparison` | [Comparison](../data_types/comparison.md) | | How the saturation level should be compared to the specified value.
`compare_to` | [Float](../data_types/float.md) | | Which value the saturation level should be compared to.

### Example:
```json
"condition": {
    "type": "origins:saturation_level",
    "comparison": "==",
    "compare_to": 0
}
```
This example checks if the player's saturation level reaches 0.