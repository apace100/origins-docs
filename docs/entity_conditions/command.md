---
title: Command
date: 2021-04-04
---
# Command

[Entity Condition](../entity_conditions.md).

Compares the result of a command to a specified value.

Type ID: `origins:command`

### Fields:

Field  | Type | Default | Description
-------|------|---------|-------------
`command` | [String](../data_types/string.md) | |  Command to run.
`comparison` | [Comparison](../data_types/comparison.md) | |  How to compare the command's result to the specified value.
`compare_to` | [Integer](../data_types/integer.md) | | Which value to compare the command's result to.

### Example:
```json
"condition": {
    "type": "origins:command",
    "command": "execute if score @s objective1 = @s objective2",
    "comparison": "==",
    "compare_to": 1
}
```
This example checks if the entity has the same score in the `objective1` and `objective2` scoreboard objectives.