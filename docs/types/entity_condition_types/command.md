---
title: Command (Entity Condition Type)
date: 2021-04-04
---

# Command

[Entity Condition Type](../entity_condition_types.md)

Compares the result of a command to a specified value.

Type ID: `origins:command`

!!! caution

    This condition is only effective server-side. That means client-side power types such as [`origins:climbing`](../power_types/climbing.md), [`origins:entity_glow`](../power_types/entity_glow.md), [`origins:shader`](../power_types/shader.md), etc. won't work with this.

### Fields:

Field  | Type | Default | Description
-------|------|---------|-------------
`command` | [String](../data_types/string.md) | |  The command to execute.
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