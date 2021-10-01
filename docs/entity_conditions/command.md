---
title: Command
date: 2021-04-04
---
# Command

[Entity Condition](../entity_conditions.md).

Compares the result of a command to a specified value.

**Note:** this condition is only effective on the server-side. That means client-based power types such as [`origins:climbing`](../power_types/climbing.md), [`origins:entity_glow`](../power_types/entity_glow.md), [`origins:shader`](../power_types/shader.md), etc. won't work with this.

Type ID: `origins:command`

### Fields:

Field  | Type | Default | Description
-------|------|---------|-------------
`command` | [String](../data_types/string.md) | |  Command to run.
`comparison` | [Comparison](../data_types/comparison.md) | |  How to compare the command's result to the specified value.
`compare_to` | [Integer](../data_types/integer.md) | | Which value to compare the command's result to.
`permission_level` | [Integer](../data_types/integer.md) | 4 | The permission level to use for the command. 0 is a "survival player", anything higher emulates some form of operator. See [Minecraft Wiki (op-permission-level)](https://minecraft.fandom.com/wiki/Server.properties#op-permission-level) for details.

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