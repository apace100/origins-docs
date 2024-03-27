---
title: Amount (Damage Condition Type)
date: 2021-04-04
---

# Amount

[Damage Condition Type](../damage_condition_types.md)

Checks whether the damage is of a specified amount.

Type ID: `origins:amount`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`comparison` | [Comparison](../data_types/comparison.md) | |  Determines how the amount of damage should be compared to the specified value.
`compare_to` | [Float](../data_types/float.md) | | The value at which the amount of damage will be compared to.


### Examples

```json
"damage_condition": {
    "type": "origins:amount",
    "comparison": "==",
    "compare_to": 4
}
```

This example will check if the damage dealt/taken is equal to 2 hearts.
