---
title: Scoreboard (Entity Condition)
date: 2021-04-04
---
# Scoreboard

[Entity Condition](../entity_conditions.md).

Compares the value of a scoreboard objective on the player to a specified value.

Type ID: `origins:scoreboard`

!!! note

    If the player does not have the the scoreboard objective, this condition would always return false (even if `"=/="` is run). You can then use the `"=/="` comparison in combination with the `"=="` comparison to test if the player does not have this objective set (for example, if a player has newly joined a world or had their objectives reset).

!!! caution

    This condition is only effective server-side. That means client-side power types such as [`origins:climbing`](../power_types/climbing.md), [`origins:entity_glow`](../power_types/entity_glow.md), [`origins:shader`](../power_types/shader.md), etc. won't work with this.

### Fields:

Field  | Type | Default | Description
-------|------|---------|-------------
`objective` | [String](../data_types/comparison.md) | | The name of the scoreboard objective to retrieve the value from and compare.
`comparison` | [Comparison](../data_types/comparison.md) | | How to compare the objective's value to the specified value.
`compare_to` | [Integer](../data_types/integer.md) | | Which value to compare the objective's value to.

### Example:

```json
"condition": {
    "type": "origins:scoreboard",
    "objective": "obj",
    "comparison": ">",
    "compare_to": 3
}
```

This condition will activate whenever the player has a value greater than 3 on the scoreboard objective "obj".
