---
title: Air (Entity Condition Type)
date: 2021-04-04
---

# Air

[Entity Condition Type](../entity_condition_types.md)

Checks how much breath / air / bubble the entity has at the moment.

Type ID: `origins:air`

!!! note

    Players (and most mobs) have a max value of 300 ticks, whilst dolphins have a max value of 4800 ticks. Axolotls, on the other hand, have a max value of 6000 ticks.

    In order to get the value of a single bubble, you can divide the max value by 10. (`max / 10 = value`)


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`comparison` | [Comparison](../data_types/comparison.md) | |  Determines how the breath / air / bubble (in ticks) the entity has should be compared to the specified value.
`compare_to` | [Integer](../data_types/integer.md) | | The value at which the breath / air / bubble (in ticks) the entity has will be compared to.


### Examples

```json
"condition": {
    "type": "origins:air",
    "comparison": "==",
    "compare_to": 0
}
```

This example will check if the player has no breath / air / bubbles left.
