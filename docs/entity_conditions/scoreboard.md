---
title: Scoreboard
date: 2021-04-04
---
# Scoreboard

[Entity Condition](../entity_conditions.md).

Compares the value of a scoreboard objective on the entity to a specified value.

**Note 1**: If the entity does not have the scoreboard objective, this condition would always return false (even if != is run). You can then use the != comparison in combination with the == comparison to test if the entity does not have this objective set (for example if a player has newly joined a world or had their objectives reset).

**Note 2**: Due to the nature of scoreboards, this condition is only effective on the server-side. That means client-based powers, such as triggering active powers, climbing, or making entities glow, won't work with this.

Type ID: `origins:scoreboard`

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

This condition will activate whenever the entity has a value greater than 3 on the scoreboard objective "obj".
